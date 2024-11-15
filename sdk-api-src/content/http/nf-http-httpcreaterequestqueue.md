---
UID: NF:http.HttpCreateRequestQueue
title: HttpCreateRequestQueue function (http.h)
description: Creates a new request queue or opens an existing request queue.
helpviewer_keywords: ["HTTP_CREATE_REQUEST_QUEUE_FLAG_CONTROLLER","HTTP_CREATE_REQUEST_QUEUE_FLAG_OPEN_EXISTING","HttpCreateRequestQueue","HttpCreateRequestQueue function [HTTP]","http.httpcreaterequestqueue","http/HttpCreateRequestQueue"]
old-location: http\httpcreaterequestqueue.htm
tech.root: http
ms.assetid: a0f4112e-db81-4eda-afeb-d00117f7240c
ms.date: 12/05/2018
ms.keywords: HTTP_CREATE_REQUEST_QUEUE_FLAG_CONTROLLER, HTTP_CREATE_REQUEST_QUEUE_FLAG_OPEN_EXISTING, HttpCreateRequestQueue, HttpCreateRequestQueue function [HTTP], http.httpcreaterequestqueue, http/HttpCreateRequestQueue
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - HttpCreateRequestQueue
 - http/HttpCreateRequestQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpCreateRequestQueue
---

# HttpCreateRequestQueue function


## -description

The <b>HttpCreateRequestQueue</b> function creates a new request queue or opens an existing request queue.

 This function replaces the HTTP version 1.0 <a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a> function.

## -parameters

### -param Version [in]

An HTTPAPI_VERSION structure indicating the request queue version. For  version 2.0, declare an instance of the structure and set it to the predefined value HTTPAPI_VERSION_2 before passing it to <b>HttpCreateRequestQueue</b>.

The version must be 2.0; <b>HttpCreateRequestQueue</b> does not support  version 1.0 request queues.

### -param Name [in, optional]

The name of the request queue. The length, in bytes, cannot exceed MAX_PATH.

  The optional name parameter allows other processes to access the request queue by name.

### -param SecurityAttributes [in, optional]

A pointer to the <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that contains the  access permissions for the request queue.

This parameter must be <b>NULL</b> when opening an existing request queue.

### -param Flags [in, optional]

The flags parameter defines the scope of the request queue. This parameter can be one or more of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_CREATE_REQUEST_QUEUE_FLAG_CONTROLLER"></a><a id="http_create_request_queue_flag_controller"></a><dl>
<dt><b>HTTP_CREATE_REQUEST_QUEUE_FLAG_CONTROLLER</b></dt>
</dl>
</td>
<td width="60%">
The handle to the request queue created using this flag cannot be used to perform I/O operations. This flag can be set only when the request queue  handle is created.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_CREATE_REQUEST_QUEUE_FLAG_OPEN_EXISTING"></a><a id="http_create_request_queue_flag_open_existing"></a><dl>
<dt><b>HTTP_CREATE_REQUEST_QUEUE_FLAG_OPEN_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
 The <b>HTTP_CREATE_REQUEST_QUEUE_FLAG_OPEN_EXISTING</b> flag allows applications to open an existing request queue by name and retrieve the request 	queue handle. The <i>pName</i> parameter  must contain a valid request queue name; it cannot be <b>NULL</b>.

</td>
</tr>
</table>

### -param RequestQueueHandle [out]

A pointer to a variable that receives a handle to the request queue.  This parameter must contain a valid pointer; it cannot be <b>NULL</b>.

## -returns

If the function succeeds, it returns <b>NO_ERROR</b>

If the function fails, it returns one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The <i>Version</i> parameter contains an invalid version.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The length, in bytes, of the request queue name cannot exceed MAX_PATH.

The <i>pSecurityAttributes</i> parameter must be <b>NULL</b> when opening an existing request queue.

The <b>HTTP_CREATE_REQUEST_QUEUE_FLAG_CONTROLLER</b> can only be set when the request queue is created.

The <b>HTTP_CREATE_REQUEST_QUEUE_FLAG_OPEN_EXISTING</b> can only be set when the application has permission to open an existing request queue. In this case, the <i>pReqQueueHandle</i> parameter must be a valid pointer, and the <i>pName</i> parameter must contain a valid request queue name; it cannot be <b>NULL</b>.

The <i>pReqQueueHandle</i> parameter returned by <a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a>  is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The <i>pName</i> parameter conflicts with an existing request queue  that contains an identical name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process does not have a permission to open the request queue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DLL_INIT_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The application has not called <a href="/windows/desktop/api/http/nf-http-httpinitialize">HttpInitialize</a> prior to calling <a href="/windows/desktop/api/http/nf-http-httpcreaterequestqueue">HttpCreateRequestQueue</a>.

</td>
</tr>
</table>

## -remarks

The HTTP Server API supports existing applications using the version 1.0 request queues, however, new development with the HTTP Server API should use <b>HttpCreateRequestQueue</b> to create request queues; <a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a> should not be used. The version 2.0 API are only compatible with the version 2.0 request queues created by <b>HttpCreateRequestQueue</b>.

The HTTP version 2 request queues require manual configuration; the application must create the URL Groups and associate one or more URL Group with the request queue by calling <a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a> with the <b>HttpServerBindingProperty</b>. The application configures the request queue by calling <a href="/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a> with the    desired configuration in the <i>Property</i> parameter. For more information about creating and configuring URL groups, see  <a href="/windows/desktop/api/http/nf-http-httpcreateurlgroup">HttpCreateUrlGroup</a> and  <b>HttpSetUrlGroupProperty</b>.

Security attributes may be supplied in <i>pSecurityAttributes</i> parameter only when the request queue is created. Only the  application that creates the request queue can set Access Control Lists (ACLs) on the request queue handle to allow processes (other than the creator application) permission to open, receive requests, and send responses on the request queue handle. By default, applications are not allowed to open a request queue unless they have been granted permission in the ACL.

The creator process can optionally use the <b>HTTP_CREATE_REQUEST_QUEUE_FLAG_CONTROLLER</b> flag to indicate that it does not want to receive http requests. 

<b>HttpCreateRequestQueue</b> allows applications to open an existing request queue with the <b>HTTP_CREATE_REQUEST_QUEUE_FLAG_OPEN_EXISTING</b> flag and retrieve the handle to the request queue. Non-controller applications can use this handle to perform HTTP I/O operations. Only the application that creates the request queue can set properties on it by calling the <a href="/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>.

The handle to the request queue created by <b>HttpCreateRequestQueue</b> must be closed by calling <a href="/windows/desktop/api/http/nf-http-httpcloserequestqueue">HttpCloseRequestQueue</a> before the application terminates or when the session is no longer required.

Applications must call <a href="/windows/desktop/api/http/nf-http-httpinitialize">HttpInitialize</a> prior to calling <b>HttpCreateRequestQueue</b>.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpcloserequestqueue">HttpCloseRequestQueue</a>



<a href="/windows/desktop/api/http/nf-http-httpcreatehttphandle">HttpCreateHttpHandle</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryrequestqueueproperty">HttpQueryRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpshutdownrequestqueue">HttpShutdownRequestQueue</a>
