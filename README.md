Dublin Traceroute is a NAT-aware multipath traceroute tool.

And this page is just informational. **Read more at https://dublin-traceroute.net** .

Dublin Traceroute has a blog, with articles on how to make the best out of it. Check it out at [blog.dublin-traceroute.net](https://blog.dublin-traceroute.net).

Dublin Traceroute has also Python bindings, that will let you:
* use Dublin Traceroute from Python code
* generate graphical visualizations of your multipath traceroutes
* do statistical analysis using Pandas

See [python-dublin-traceroute](https://github.com/insomniacslk/python-dublin-traceroute) for more information.

Feedback is very welcome! You can [open a new issue](https://github.com/insomniacslk/dublin-traceroute/issues/new/choose), or contact me directly, see https://insomniac.slackware.it for contact details.

But, in a few words, you can run traceroutes in multi-path networks (i.e. with ECMP load-balancing enabled), recognize NATs, have nice diagrams like the one below, export to JSON, and do this with a command-line tool, a C++ library or a Python library.

![dublin-traceroute example](https://raw.githubusercontent.com/arbal/dublin-traceroute/master/docs/traceroute_8.8.8.8.png)


### Docker Example

*For this fork, here an example using the [arbal/dublin-traceroute](https://hub.docker.com/r/arbal/dublin-traceroute) Docker image ( built from [https://github.com/arbal/dublin-traceroute](https://github.com/arbal/dublin-traceroute) ).*

#### Dublin Traceroute to wikipedia.org using Docker:
`docker run arbal/dublin-traceroute:latest bash -c "{ dublin-traceroute wikipedia.org --output-file /dtr.json && python3 -m dublintraceroute plot /dtr.json; } &>/dev/null && cat /dtr.json.png" > wikipedia.org_dublin-traceroute.png`

![dublin-traceroute example using docker](https://raw.githubusercontent.com/arbal/dublin-traceroute/master/docs/wikipedia.org_dublin-traceroute.png)
