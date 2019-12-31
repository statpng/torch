# torch


#### show the dimension of TochTensor class
TorchTensor.size()

#### reshape TorchTensor
target.view

#### generate a random number
torch.randn(1)

#### set a randomseed for each cpu and gpu
torch.manual_seed(1514780611)
torch.cuda.manual_seed_all(7053313890570024)

#### set an object as a criterion like MSELoss
criterion = nn.MSELoss()

#### make the gradients to be zeros because backward of PyTorch accumulates the gradients on their process.
#### Probabily, you don't want to mix up the gradients between minibatches
net.zero_grad()     # zeroes the gradient buffers of all parameters

print('conv1.bias.grad before backward')
print(net.conv1.bias.grad)

loss.backward()

print('conv1.bias.grad after backward')
print(net.conv1.bias.grad)
