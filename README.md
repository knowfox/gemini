# Gemini

[Gemini protocol](https://gitlab.com/gemini-specification/protocol/-/blob/master/specification.gmi) and [Titan Protocl](https://communitywiki.org/wiki/Titan) GO package for the server using [net/http](https://pkg.go.dev/net/http) style API.

The package was created after attempt to use a couple of existing libraries for the server side and not finding those satisfactory in terms of exposed API.

The package follows core design pattern used in standard [net/http](https://pkg.go.dev/net/http) package.  API correlation made it possible to adapt [julienschmidt/httprouter](https://github.com/julienschmidt/httprouter) package to GEMINI protocol in [geminirouter](https://github.com/kulak/geminirouter) package.

Titan protocol tested with [Lagrange](https://git.skyjake.fi/gemini/lagrange) browser.

## Example Server

To run server one needs to generate appropriate server certificate.

Run example server:

    make run

## Known Issues

`getRequest` function reading request bytes is functional, but seems to be ineficient.
