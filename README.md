# demo_nn_compress
This is a demo of compressing AlexNet from 233MB to 8.9MB without any accyracy loss.

Usage:
    export CAFFE_ROOT=$your caffe root$
    python decode.py bvlc_alexnet_deploy.prototxt compress.net $CAFFE_ROOT/alexnet.caffemodel 
    cd $CAFFE_ROOT
    ./build/tools/caffe test --model=models/bvlc_alexnet/train_val.prototxt \
    --weights=alexnet.caffemodel --iterations=1000 --gpu 0
