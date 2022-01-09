# WordPressTrial

#### AWSでサーバーを立てました　http://nobuhara.tk/wordpress

#### サーバ側でhttps対応後、wordpressの表示が崩れるので、下記設定が必要
- wp-config.phpに追加
~~~
if (isset($_SERVER['HTTP_X_FORWARDED_PROTO']) && $_SERVER['HTTP_X_FORWARDED_PROTO'] == 'https')
    $_SERVER['HTTPS'] = 'on';
~~~
