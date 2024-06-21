# Attack-Detection-on-IoT-Devices-with-KAN
DataSet : https://www.kaggle.com/datasets/francoisxa/ds2ostraffictraces

Faster-KAN : https://github.com/AthanasiosDelis/faster-kan

## Kolmogorov-Arnold-Network (KAN) :-
Kolmogorov-Arnold-Network is a approach to neural network inspired by Kolmogorov-Arnold representation theorem. Unlike MLP, KAN utlizes the concept of updatable activation function rather than fixed activation function which allows them to fulfil the functionality of both weights and activation functions. These activations functions are present at edges rather than nodes. All in all, KANs offer a better accuracy and performance along with better iterpretability but lacks on the side of computational efficiency.

$$MLP : f(x) = \sum_{i=1}^{N(e)}a_{i}\sigma(w_{i}.x + b_{i})$$

$$KAN : f(x) = f(x_{1},...,x_{n}) = ∑_{q=1}^{2n + 1}𝚽_{q}(∑_{p=1}^{n}Φ_{q, p}(x_{p}))$$

For better computational efficiency, I utilized faster-kan by Athanasios Delis which makes use Radial Basis Function, and functions capable of reflectional symmetry.
### Guassian-Radial-Basis-Function (RBF):-
A Radial Basis Function is a real-valued function, the value of which depends only on the distance from the origin. Among various types of Radial Basis Function, Guassian Radial Basis Function is the most common.
* $b_{i}(u) = e^{(-(u - u_{i})^{2}/h)}$
### Reflextional-Switch-Activation Function (RSWAF):-
Uses function which have reflextionary symmetry, allows us to retain performance while reducing computation time.
* $b_{i}(u) = 1 - (tanh((u - u_{i})/h))^{2}$
