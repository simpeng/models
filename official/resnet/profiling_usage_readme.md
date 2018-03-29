command:

 python cifar10_main.py --data_dir ~/dataset/resnet_cifar10 --profiling_dir profiling_tmp --train_epochs 1 --epochs_between_evals 1 --max_train_steps 10


why need specify:
- train_epochs and epochs_between_evals: because the first // second will be the calcuated as iternation count of calling train and eval functions. 


after run, we got proling file in the profiling_dir, then use:
bazel-bin/tensorflow/core/profiler/profiler following https://github.com/tensorflow/tensorflow/tree/master/tensorflow/core/profiler#features, to get what you want. 


