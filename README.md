Fork of http://bitbucket.org/ianb/webtest
Current Version: 1.2.4

Old API

    resp = app.post('/deliverance/redirects?remove',
                    '[{"path": "/blahblah"}]', status=400)

New API (borrowed from [Requests](http://docs.python-requests.org/en/latest/index.html)

    resp = app.post('/deliverance/redirects?remove',
                    data={"path": "/blahblah"})
    assert resp.status_code == 400

Doesn't look like much, but I find it much easier to use.

