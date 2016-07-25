# ImmersiveStatusBar

沉浸式状态栏，状态栏与图片融合

	public void setTranslucent()
    {
        if(Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT)
        {
            this.getWindow().addFlags(WindowManager.LayoutParams.FLAG_TRANSLUCENT_STATUS);
            ViewGroup rootView = (ViewGroup) ((ViewGroup) this.findViewById(android.R.id.content)).getChildAt(0);
            rootView.setFitsSystemWindows(true);

        }
    }

this.getWindow().addFlags(WindowManager.LayoutParams.FLAG_TRANSLUCENT_STATUS);这句话就是设置为透明状态栏
rootView.setFitsSystemWindows(true);是设置是否考虑标题栏进去，如果不设置或者设置为false,是这样的
![](http://i.imgur.com/0kO0ozH.png)

设置为true后，就正常了。

![](http://i.imgur.com/aDXM52s.png)
