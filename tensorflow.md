# Tensorflow 快速手册

### Import
	import tensorflow as tf

### Basic

	tf.VERSION	# tf版本

### Eager
	#启用eager
	tf.enable_eager_execution()

	# 判断是否启用了eager，返回 True/False
	tf.executing_eagerly()

### Dataset

	# 加载内存中的数据
	d1 = [[1, 2], [0, 4], [5, 3]]
	dataset = tf.data.Dataset.from_tensor_slices(d1)
	dataset = tf.data.Dataset.from_tensors(d1)
	
	# 随机生成
	dataset_r = tf.data.Dataset.from_tensor_slices(tf.random_uniform([3, 10], 
		maxval=10, dtype=tf.int32))
	
	# 生成range
	dataset_range = tf.data.Dataset.range(20)

