---
UID: NF:msxml6.IXMLHTTPRequest2.Open
title: IXMLHTTPRequest2::Open (msxml6.h)
description: Initializes an IXMLHTTPRequest2 request and specifies the method, URL, and authentication information for the request. After calling this method, you must call the Send method to send the request and data, if any, to the server.
helpviewer_keywords: ["IXMLHTTPRequest2 interface [XMLHttpRequest2]","Open method","IXMLHTTPRequest2.Open","IXMLHTTPRequest2::Open","Open","Open method [XMLHttpRequest2]","Open method [XMLHttpRequest2]","IXMLHTTPRequest2 interface","ixhr2.ixmlhttprequest2_open","msxml6/IXMLHTTPRequest2::Open"]
old-location: ixhr2\ixmlhttprequest2_open.htm
tech.root: ixhr2
ms.assetid: 8723F24B-0739-44D6-8443-1A378B585F42
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest2 interface [XMLHttpRequest2],Open method, IXMLHTTPRequest2.Open, IXMLHTTPRequest2::Open, Open, Open method [XMLHttpRequest2], Open method [XMLHttpRequest2],IXMLHTTPRequest2 interface, ixhr2.ixmlhttprequest2_open, msxml6/IXMLHTTPRequest2::Open
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps],MSXML 6.0 and later
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml6.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXMLHTTPRequest2::Open
 - msxml6/IXMLHTTPRequest2::Open
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest2.Open
---

# IXMLHTTPRequest2::Open


## -description

Initializes an <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a> request and specifies the method, URL, and authentication information for the request.  After calling this method, you must call the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-send">Send</a>  method to send the request and data, if any, to the server.

## -parameters

### -param pwszMethod [in]

The HTTP method used to open the connection, such as <b>GET</b> or <b>POST</b>. For XMLHTTP, this parameter is not case-sensitive.

### -param pwszUrl [in]

The requested URL. This must be an absolute URL, such as "http://Myserver/Mypath/Myfile.asp".

### -param pStatusCallback [in, optional]

A callback interface implemented by the app that is to receive callback events. 

When the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-send">Send Method</a> is successful, the methods on this interface are called to process the response or other events.

### -param pwszUserName [in, optional]

The name of the user for authentication. If this parameter is a Null and the site requires authentication, credentials will be managed by Windows, including displaying a logon UI, unless disabled by <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a>.

### -param pwszPassword [in, optional]

The password for authentication. This parameter is ignored if the <i>pwszUserName</i> parameter is Null or missing.

### -param pwszProxyUserName [in, optional]

The name of the user for authentication on the proxy server. If this parameter is a Null or empty string and the site requires authentication, credentials will be managed by Windows, including displaying a logon UI, unless disabled by <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a>.

### -param pwszProxyPassword [in, optional]

The password for authentication on the proxy server. This parameter is ignored if the <i>pwszProxyUserName</i> parameter is Null or missing.

## -returns

Returns <b>S_OK</b> on success.

## -remarks

Although this method accepts credentials passed via parameter, these credentials are not automatically sent to the server on the first request. The <i>pwszUserName</i> and <i>pwszPassword</i> parameters are not sent to the server unless the server challenges the client for credentials with a 401 - Unauthorized response.


#### Examples


``` syntax
//
// Create and initialize an IXMLHTTPRequest2 object
//
hr = CoCreateInstance(CLSID_FreeThreadedXMLHTTP60,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spXHR));

//
//Create and initialize an IXMLHTTPRequest2Callback object
//
hr = MakeAndInitialize<CXMLHttpRequest2Callback>(&spXhrCallback);

hr = spXHR->Open(L"GET",              // Method.
                 pcwszUrl,            // Url.
                 spXhrCallback.Get(), // Callback.
                 NULL,                // Username.
                 NULL,                // Password.
                 NULL,                // Proxy username.
                 NULL);               // Proxy password.

//
//Send the GET request
//
hr = spXHR->Send(NULL, 0);

hr = spXhrCallback->WaitForComplete(&dwStatus);
```

For the complete examples, see the <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/XmlHttpRequest2GetRequest">XML HTTP Request 2 GET  sample</a> and  <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/XmlHttpRequest2PostRequest">XML HTTP Request 2 POST  sample</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback Interface</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-send">Send Method</a>
