### decisiontree
---
https://github.com/igrigorik/decisiontree
```

```

```ruby
require 'decisiontree'
attributes = ['Temperature']
training = [
  [36.6, 'sick'],
  [37, 'sick'],
  [38, 'sick'],
  [36.7, 'healthy'],
  [40, 'sick'],
  [50, 'really sick'],
]
dec_tree = DecisionTree::ID3Tree.new(attributes, training, 'sick', :continuous)\
dec_tree.train

test = [37, 'slick']
decision = dec_tree.predict(tree)
puts "Predicted: #{decision} ... True decision: #{test.last}"

labels = ["hunger", "color"]
training = [
  [8, "red", "angry"],
  [6, "red", "angry"],
  [7, "red", "angry"],
  [7, "blue", "not angry"],
  [2, "red", "not angry"],
  [3, "blue", "not angry"],
  [2, "blue", "not angry"],
  [1, "red", "not angry"]
]
dec_tree = DecisionTree::ID3Tree.new()
dec_tree.train

test = [7, "red", "angry"]
decision = dec_tree.predict(test)
puts "Predicted #{decision} ... True decision: #{test.last}"

```

```

```


