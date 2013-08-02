## Wildfly Application Server running on OpenShift##

1. Create an OpenShift DIY application.
```
$ rhc app create wildfly diy
```

2. Add git remote and pull the sourcecode
```
$ git remote add upstream -m master https://github.com/shekhargulati/wildfly-openshift-quickstart.git
$ git pull -s recursive -X theirs upstream master
```

3. Git push source code
```
$ git push
```

4. Wildly application server will be accessible at http://wildfly-{domain-name}.rhcloud.com

5. To add admin user, ssh into OpenShift application gear using <code>rhc ssh</code> and then run add-user.sh file. Enter username and password.
```
$ cd $OPENSHIFT_DATA_DIR/wildfly-8.0.0.Alpha3
$ sh add-user.sh
```

6. Sample WebSocket application will be running at http://wildfly-{domain-name}.rhcloud.com/websocket-reverse-echo-example. The sample example github repository is here https://github.com/shekhargulati/websocket-reverse-echo-example.
