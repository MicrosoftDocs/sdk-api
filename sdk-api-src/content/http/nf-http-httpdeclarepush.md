---
UID: NF:http.HttpDeclarePush
title: HttpDeclarePush function
author: windows-sdk-content
description: Declares a resource-to-subresource relationship to use for an HTTP server push. HTTP.sys then performs an HTTP 2.0 server push for the given resource, if the underlying protocol, connection, client, and policies allow the push operation.
old-location: http\httpdeclarepush.htm
old-project: http
ms.assetid: 02844D45-01B2-497B-83D6-8FEB904CF2FE
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: HttpDeclarePush, HttpDeclarePush function [HTTP], http.httpdeclarepush, http/HttpDeclarePush
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: HTTP_VERB, *PHTTP_VERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - httpapi.dll
api_name:
 - HttpDeclarePush
product: Windows
targetos: Windows
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# HttpDeclarePush function


## -description


Declares a resource-to-subresource relationship to  use for an HTTP     server push. HTTP.sys then performs an HTTP 2.0 server push for the given     resource, if the underlying protocol, connection, client, and policies     allow the push operation.


## -parameters




### -param RequestQueueHandle [in]

The handle to an HTTP.sys request queue that the  <a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> function returned.


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

If the function fails, it returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.




## -remarks



You should call <b>HttpDeclarePush</b> before you send any response bytes that would cause the client to discover the subresource itself.  Failure to observe this order results in a race between the server that is pushing the resource and the client that is  retrieving the resources, which can waste bandwidth.
The server application should only use <b>HttpDeclarePush</b> to push resources that the server application is highly confident are needed and not already cached by the client.  If the server application pushes other resources, unnecessary use of bandwidth and CPU may occur.





## -see-also




<a href="https://msdn.microsoft.com/a87b9c9c-cba1-4453-a300-7af35da944c9">HTTP_REQUEST_HEADERS</a>



<a href="https://msdn.microsoft.com/4aa36eab-eff2-4caa-9bad-15c534c5a5a0">HTTP_VERB</a>



<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a>
 

 

