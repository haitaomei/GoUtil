# A lazy way to set up https server
1. Config tls/generate_cert.go, and run it to generate ``cert.pem`` and ``key.pem``. Note that, don't forget to add hostname to /etc/hots if using synthetic domain names

2. server/httpsServer.go will use ``cert.pem`` and ``key.pem`` to start server

3. request.go use ``cert.pem`` as the caCert to connect