# luban
图片压缩

        Luban.get(this)
                .load(file)                     //传人要压缩的图片
                .putGear(Luban.THIRD_GEAR)      //设定压缩档次，默认三挡
                .setCompressListener(new OnCompressListener() { //设置回调

                    @Override
                    public void onStart() {
                      
                        //TODO 压缩开始前调用，可以在方法内启动 loading UI

                    }
                    @Override
                    public void onSuccess(File file) {
                        //TODO 压缩成功后调用，返回压缩后的图片文件
                 
                       imageView.setImageBitmap(BitmapFactory.decodeFile(file.getAbsolutePath()));


                    }

                    @Override
                    public void onError(Throwable e) {
                        //TODO 当压缩过去出现问题时调用
                    }
                }).launch();    //启动压缩
