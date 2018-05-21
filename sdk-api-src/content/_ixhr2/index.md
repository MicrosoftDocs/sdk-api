---
UID: TP:ixhr2
ms.assetid: 1bcd6a5a-1ca6-357d-9684-cbdeef45fb68
ms.author: windowsdriverdev
ms.date: 05/21/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
archived: true
---

# XML HTTP Extended Request



Overview of the XML HTTP Extended Request technology.

To develop XML HTTP Extended Request, you need these headers:

 * [msxml6.h](..\msxml6\index.md)

For the programming guide, see [XML HTTP Extended Request](https://review.docs.microsoft.com/en-us/win32-test/ixhr2).

## Structures

| Title   | Description   |
| ---- |:---- |
| [tagXHR_CERT structure](..\msxml6\ns-msxml6-tagxhr_cert.md) | Defines a buffer that points to an encoded certificate. |
| [tagXHR_COOKIE structure](..\msxml6\ns-msxml6-tagxhr_cookie.md) | Defines a cookie that you can add to the HTTP cookie jar by calling the SetCookie method or retrieve from the HTTP cookie jar by calling the GetCookie method. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [_XHR_AUTH enumeration](..\msxml6\ne-msxml6-_xhr_auth.md) | Specifies whether to allow authentication to be used to connect to a proxy or to connect to the HTTP server. |
| [_XHR_CERT_ERROR_FLAG enumeration](..\msxml6\ne-msxml6-_xhr_cert_error_flag.md) | Defines flags that indicate server certificate errors during SSL negotiation with the server by handling the OnServerCertificateReceived method on the IXMLHTTPRequest3Callback interface. |
| [_XHR_CERT_IGNORE_FLAG enumeration](..\msxml6\ne-msxml6-_xhr_cert_ignore_flag.md) | Defines flags that you can assign to an outgoing HTTP request to ignore certain certificate errors by calling the SetProperty method on the IXMLHTTPRequest3 interface. |
| [_XHR_COOKIE_FLAG enumeration](..\msxml6\ne-msxml6-_xhr_cookie_flag.md) | Defines a set of flags that you can assign to a cookie in the HTTP cookie jar by calling the SetCookie method or query from the HTTP cookie jar by calling the GetCookie method. |
| [_XHR_COOKIE_STATE enumeration](..\msxml6\ne-msxml6-_xhr_cookie_state.md) | Specifies the state of the cookie. |
| [_XHR_CRED_PROMPT enumeration](..\msxml6\ne-msxml6-_xhr_cred_prompt.md) | Specifies whether to allow credential prompts to the user for authentication. |
| [_XHR_PROPERTY enumeration](..\msxml6\ne-msxml6-_xhr_property.md) | Defines properties that you can assign to an outgoing HTTP request by calling the SetProperty method. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IXMLHTTPRequest2 interface](..\msxml6\nn-msxml6-ixmlhttprequest2.md) | Provides the methods and properties needed to configure and send HTTP requests and use callbacks to receive notifications during HTTP response processing. Note  This interface is supported on Windows Phone 8.1.  . |
| [IXMLHTTPRequest2Callback interface](..\msxml6\nn-msxml6-ixmlhttprequest2callback.md) | Defines callbacks that notify an application with an outstanding IXMLHTTPRequest2 request of events that affect HTTP request and response processing. Note  This interface is supported on Windows Phone 8.1.  . |
| [IXMLHTTPRequest3 interface](..\msxml6\nn-msxml6-ixmlhttprequest3.md) | Provides the methods and properties needed to configure and send HTTP requests and use callbacks to receive notifications during HTTP response processing. |
| [IXMLHTTPRequest3Callback interface](..\msxml6\nn-msxml6-ixmlhttprequest3callback.md) | Defines callbacks that notify an application with an outstanding IXMLHTTPRequest3 request of events that affect HTTP request and response processing. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IXMLHTTPRequest2::Abort](..\msxml6\nf-msxml6-ixmlhttprequest2-abort.md) | Cancels the current HTTP request. |
| [IXMLHTTPRequest2::GetAllResponseHeaders](..\msxml6\nf-msxml6-ixmlhttprequest2-getallresponseheaders.md) | Retrieves the values of all the HTTP response headers. |
| [IXMLHTTPRequest2::GetCookie](..\msxml6\nf-msxml6-ixmlhttprequest2-getcookie.md) | Gets a cookie associated with the specified URL from the HTTP cookie jar. |
| [IXMLHTTPRequest2::GetResponseHeader](..\msxml6\nf-msxml6-ixmlhttprequest2-getresponseheader.md) | Retrieves the value of an HTTP header from the response headers. |
| [IXMLHTTPRequest2::Open](..\msxml6\nf-msxml6-ixmlhttprequest2-open.md) | Initializes an IXMLHTTPRequest2 request and specifies the method, URL, and authentication information for the request. After calling this method, you must call the Send method to send the request and data, if any, to the server. |
| [IXMLHTTPRequest2::Send](..\msxml6\nf-msxml6-ixmlhttprequest2-send.md) | Sends an HTTP request to the server asynchronously. On success, methods on the IXMLHTTPRequest2Callback interface implemented by the app are called to process the response. |
| [IXMLHTTPRequest2::SetCookie](..\msxml6\nf-msxml6-ixmlhttprequest2-setcookie.md) | Sets a cookie associated with the specified URL in the HTTP cookie jar. |
| [IXMLHTTPRequest2::SetCustomResponseStream](..\msxml6\nf-msxml6-ixmlhttprequest2-setcustomresponsestream.md) | Provides a custom stream to replace the standard stream for receiving an HTTP response. |
| [IXMLHTTPRequest2::SetProperty](..\msxml6\nf-msxml6-ixmlhttprequest2-setproperty.md) | Sets a property on an outgoing HTTP request. |
| [IXMLHTTPRequest2::SetRequestHeader](..\msxml6\nf-msxml6-ixmlhttprequest2-setrequestheader.md) | Specifies the name of an HTTP header to be sent to the server along with the default request headers. |
| [IXMLHTTPRequest2Callback::OnDataAvailable](..\msxml6\nf-msxml6-ixmlhttprequest2callback-ondataavailable.md) | Occurs when a client receives part of the HTTP response data from the server. |
| [IXMLHTTPRequest2Callback::OnError](..\msxml6\nf-msxml6-ixmlhttprequest2callback-onerror.md) | Occurs when an error is encountered or the request has been aborted. |
| [IXMLHTTPRequest2Callback::OnHeadersAvailable](..\msxml6\nf-msxml6-ixmlhttprequest2callback-onheadersavailable.md) | Occurs after an HTTP request has been sent to the server and the server has responded with response headers. |
| [IXMLHTTPRequest2Callback::OnRedirect](..\msxml6\nf-msxml6-ixmlhttprequest2callback-onredirect.md) | Occurs when a client sends an HTTP request that the server redirects to a new URL. |
| [IXMLHTTPRequest2Callback::OnResponseReceived](..\msxml6\nf-msxml6-ixmlhttprequest2callback-onresponsereceived.md) | Occurs when a client has received a complete response from the server. |
| [IXMLHTTPRequest3Callback::OnClientCertificateRequested](..\msxml6\nf-msxml6-ixmlhttprequest3callback-onclientcertificaterequested.md) | Occurs when a client receives a request for a client certificate during SSL negotiation with the server. |
| [IXMLHTTPRequest3Callback::OnServerCertificateReceived](..\msxml6\nf-msxml6-ixmlhttprequest3callback-onservercertificatereceived.md) | Occurs when a client receives certificate errors or a server certificate chain during SSL negotiation with the server. |
