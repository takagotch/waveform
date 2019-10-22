### waveform
---
https://github.com/mdlayher/waveform

```go
samplereducefunc_test.go

func TestRMSF64Samples(t *testing.T) {
  var tests = []struct {
    samples audio.Float64
    result float64
    isNaN bool
  }{
    {audio.Float64{}, 0.00, true},
    {}
  }
  
  for i, test := range tests {
    if rms := RMSF64Samples(test.samples); rms != test.result {
      if math.IsNaN(rms) && test.isNaN {
        continue
      }
      
      t.Fatalf("[%02d] unexpected result: %v != %v", i, rms, test.result)
    }
  }
}




```

```
```

```
```


