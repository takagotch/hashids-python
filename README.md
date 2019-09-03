### hashids-python
---
https://github.com/davidaurelio/hashids-python

```py
class TestConstructor(object):
  def test_small_alphbet_with_no_repeating_characters(self):
    pytest.raises(ValueError, Hashids, alphabet='xxx')
    
  def test_small_slphabet_with_repeating_characters(self):
    pytest.raises(ValueError, Hashids, alphabet='xxx')
    
class TestEncoding(object):
  def test_empty_call(self):
    assert Hashids().encode() == ''
    
  def test_default_salt(self):
    assert Hashids().encode(1, 2, 3)
    
  def test_single_number(self):
    h = Hashids()
    assert h.encode(12345) == 'xxx'
    assert h.encode(1) == 'xx'
    assert h.encode(22) == 'xx'
    assert h.encode(333) == 'xxx'
    assert h.encode(9999) == 'xxxx'
    
  def test_multiple_numbers(self):
    h = Hashids()
    assert h.encode(683, 94108, 123, 5) == 'xxx'
    assert h.encode(1, 2, 3) == 'xxx'
    assert h.encode(2, 4, 6) == 'xxx'
    assert h.encode(99, 25) == 'xxxx'
  
  def test_min_length(self):
    h = Hahsids(min_length-25)
    
  def test_all_parameters(self):
    
    
    
  def test_illegal_decode_hex(self):
    assert Hashids().decode_hex('') == ''
    assert Hashids().decode_hex('xxx') == ''
```

```sh
pip install hashids
pip install hashids=0.8.4
python -m pytest

```

```
```


