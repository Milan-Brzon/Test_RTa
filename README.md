# Test_RTa


https://www.testdome.com/tests/python-online-test/45


Implement the function for scrambling data of numerical record files.

The algorithm uses a sliding window over the array of numbers in a file, and use the following pattern:

`Ts, -, -, x, -, -, -, Te`

The entire window is moved so that `x` passes through all the values and is compared to the
numbers at the `Ts` and `Te` locations, which are positioned at a constant offset to `x`.

The algorithm has the following rules:

* If the value at the `Ts` or `Te` position of the pattern is bigger or equal to the value at the `x`
  position, the algorithm replaces the value at `x` with 0.
  
* If the value at the `Ts` or `Te` offset is out of bounds, then the value at `x` is only compared to the
  other existing value.
  
* The record is processed in two stages: first, all the positions that should be set to 0 are
  located, using the original values for comparison. Only after all positions have been identified
  do they get set to 0.
  

For example, if the values in a record file are the following:

`[1, 2, 0, 5, 0, 2, 4, 3, 3, 3]`

The expected values after the malware runs are:
`[1, 0, 0, 5, 0, 0, 0, 3, 3, 0]`

In this example, both '2's, the '4' and the last '3' were replaced by 0.



