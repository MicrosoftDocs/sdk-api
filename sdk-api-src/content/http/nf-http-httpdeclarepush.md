---
UID: NF:http.HttpDeclarePush
title: HttpDeclarePush function (http.h)
description: Declares a resource-to-subresource relationship to use for an HTTP server push. HTTP.sys then performs an HTTP 2.0 server push for the given resource, if the underlying protocol, connection, client, and policies allow the push operation.
helpviewer_keywords: ["HttpDeclarePush","HttpDeclarePush function [HTTP]","http.httpdeclarepush","http/HttpDeclarePush"]
old-location: http\httpdeclarepush.htm
tech.root: http
ms.assetid: 02844D45-01B2-497B-83D6-8FEB904CF2FE
ms.date: 12/05/2018
ms.keywords: HttpDeclarePush, HttpDeclarePush function [HTTP], http.httpdeclarepush, http/HttpDeclarePush
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HttpDeclarePush
 - http/HttpDeclarePush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - httpapi.dll
api_name:
 - HttpDeclarePush
---

# HttpDeclarePush function


## -description

Declares a resource-to-subresource relationship to  use for an HTTP     server push. HTTP.sys then performs an HTTP 2.0 server push for the given     resource, if the underlying protocol, connection, client, and policies     allow the push operation.

## -parameters

### -param RequestQueueHandle [in]

The handle to an HTTP.sys request queue that the  <a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a> function returned.

### -param RequestId [in]

The opaque identifier of the request that is declaring the push operation. The request must be from the specified queue handle.

### -param Verb [in]

The HTTP verb to use for the push operation. The HTTP.sys push operation only supports <b>HttpVerbGET</b> and <b>HttpVerbHEAD</b>.

### -param Path [in]

The path portion of the URL for the resource being pushed.

### -param Query [in, optional]

The query portion of the URL for the resource being pushed. This          string should not include the leading question mark (?).

### -param Headers [in, optional]

The request headers for the push operation.

You should not provide a Host header, because HTTP.sys automatically generates the correct Host information.  HTTP.sys does not support cross-origin push operations, so HTTP.sys  enforces and generates Host information that matches the original client-initiated request.

The push request is not allowed to have an entity body, so you cannot include a non-zero Content-Length  header or any Transfer-Encoding header.

## -returns

If the function succeeds, it returns <b>NO_ERROR</b>.

If the function fails, it returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.

## -remarks

You should call <b>HttpDeclarePush</b> before you send any response bytes that would cause the client to discover the subresource itself.  Failure to observe this order results in a race between the server that is pushing the resource and the client that is  retrieving the resources, which can waste bandwidth.
The server application should only use <b>HttpDeclarePush</b> to push resources that the server application is highly confident are needed and not already cached by the client.  If the server application pushes other resources, unnecessary use of bandwidth and CPU may occur.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_request_headers">HTTP_REQUEST_HEADERS</a>



<a href="/windows/desktop/api/http/ne-http-http_verb">HTTP_VERB</a>



<a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a>