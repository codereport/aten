## ATen

ATen is fundamentally a tensor library, on top of which almost all other Python and C++ interfaces in PyTorch are built. It provides a core Tensor class, on which many hundreds of operations are defined. Most of these operations have both CPU and GPU implementations, to which the Tensor class will dynamically dispatch based on its type. A small example of using ATen could look as follows:

```cpp
#include <ATen/ATen.h>

at::Tensor a = at::ones({2, 2}, at::kInt);
at::Tensor b = at::randn({2, 2});
auto c = a + b.to(at::kInt);
```
This Tensor class and all other symbols in ATen are found in the at:: namespace, documented [here](https://pytorch.org/cppdocs/api/namespace_at.html#namespace-at).
