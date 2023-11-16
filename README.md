# Learning two-player games with Decision Transformers

## Project overview

Inspired by upside-down RL (UDRL; https://arxiv.org/abs/1912.02875) and Decision
Transformers (DT; https://arxiv.org/abs/2106.01345) the goal is to explore RL these
techniques in the context of two-player games. In UDRL and DT the interaction with an
environment is modelled as a sequence of action, reward, observation triplets. A
general purpose sequence model is then used to not model the strongest policy but to
model the entire distribution of actions, rewards, and observations. To maximise
performance, the model is given an observation and a large reward and asked to
generate the respective action. In a two-player setting the reward is fix (win or not win)
and the models can be pitched against each other. While initially both players aim to
win, the sequence of actions can be updated in hindsight with the actual winner and
ELO ranking in order to server as a new datapoint to train our sequence model. The
project involves the following points:
- read and understand the recent literature on RL as a sequence modelling
example
- implement two simple and fast environments for full-information games
(tic-tac-toe, checkers, chess) and partial-information games (poker, Swiss Jass,
etc).
- Experiment at small scale with general purpose sequence models (decoder-only
transformer; LSTM)
