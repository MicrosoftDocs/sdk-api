---
UID: NF:http.HttpReceiveRequestEntityBody
title: HttpReceiveRequestEntityBody function
author: windows-sdk-content
description: Receives additional entity body data for a specified HTTP request.
old-location: http\httpreceiverequestentitybody.htm
tech.root: http
ms.assetid: b4ba765f-537b-4021-9ecc-d400d9b94723
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: HTTP_RECEIVE_REQUEST_ENTITY_BODY_FLAG_FILL_BUFFER, HttpReceiveRequestEntityBody, HttpReceiveRequestEntityBody function [HTTP], _http_httpreceiverequestentitybody, http.httpreceiverequestentitybody, http/HttpReceiveRequestEntityBody
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpReceiveRequestEntityBody
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HttpReceiveRequestEntityBody function


## -description


The 
<b>HttpReceiveRequestEntityBody</b> function receives additional entity body data for a specified HTTP request.


## -parameters




### -param RequestQueueHandle [in]

The handle to the request queue from which to retrieve the specified entity body data. A request queue is created and its handle returned by a call to the 
<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="https://msdn.microsoft.com/c3741092-c23a-465f-9a65-5bcbf977fad3">HttpCreateHttpHandle</a> function.


### -param RequestId [in]

The identifier of the HTTP request that contains the retrieved entity body. This value is returned in the <b>RequestId</b> member of the 
<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a> structure by a call to the 
<a href="https://msdn.microsoft.com/ad9e80f7-04c4-4108-a7ab-40eb57d00e3b">HttpReceiveHttpRequest</a> function. This value cannot be <b>HTTP_NULL_ID</b>.


### -param Flags [in]

This parameter can be the following flag value. 

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>This parameter is reserved and must be zero.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_RECEIVE_REQUEST_ENTITY_BODY_FLAG_FILL_BUFFER"></a><a id="http_receive_request_entity_body_flag_fill_buffer"></a><dl>
<dt><b>HTTP_RECEIVE_REQUEST_ENTITY_BODY_FLAG_FILL_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the buffer will be filled with one or more  entity bodies, unless there are no remaining entity bodies to copy.

</td>
</tr>
</table>
 


### -param EntityBuffer [out]

A pointer to a buffer that receives entity-body data.


### -param EntityBufferLength [in]

The size, in bytes, of the buffer pointed to by the <i>pBuffer</i> parameter.


### -param BytesReturned [out, optional]

Optional. A pointer to a variables that receives the size, in bytes, of the entity body data returned in the <i>pBuffer</i> buffer. 




When making an asynchronous call using <i>pOverlapped</i>, set <i>pBytesReceived</i> to <b>NULL</b>. Otherwise, when <i>pOverlapped</i> is set to <b>NULL</b>, <i>pBytesReceived</i> must contain a valid memory address, and not be set to <b>NULL</b>.


### -param Overlapped [in, optional]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure; for synchronous calls, set it to <b>NULL</b>. 




A synchronous call blocks until the entity-body data has been retrieved, whereas an asynchronous call immediately returns <b>ERROR_IO_PENDING</b> and the calling application then uses 
<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For more information about using 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structures for synchronization, see <a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function is used asynchronously, a return value of <b>ERROR_IO_PENDING</b> indicates that the next request is not yet ready and is retrieved later through normal overlapped I/O completion mechanisms.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the supplied parameters are in an unusable form.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_HANDLE_EOF</b></dt>
</dl>
</td>
<td width="60%">
The specified entity body has already been completely retrieved; in this case, the value pointed to by <i>pBytesReceived</i> is not meaningful, and <i>pBuffer</i> should not be examined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DLL_INIT_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The calling application did not call 
<a href="https://msdn.microsoft.com/bc0648a9-bacf-4b09-aa4e-66aecbbdca3d">HttpInitialize</a> before calling this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.

</td>
</tr>
</table>
 




## -remarks



To retrieve an entire entity body, an application is expected to call 
<b>HttpReceiveRequestEntityBody</b>, passing in new buffers, until the function returns <b>ERROR_HANDLE_EOF</b>. As long as a buffer full of entity-body data is copied successfully and there is still more entity-body data waiting to be retrieved, the function returns <b>NO_ERROR</b>.




## -see-also




<a href="https://msdn.microsoft.com/1da9907d-a09d-41e1-aca1-9a8e2b91296f">HTTP Server API Version 1.0 Functions</a>



<a href="https://msdn.microsoft.com/49952ff5-ac8b-4192-a446-5a117f9a8e52">HTTP Server Sample Application</a>



<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a>



<a href="https://msdn.microsoft.com/ad9e80f7-04c4-4108-a7ab-40eb57d00e3b">HttpReceiveHttpRequest</a>



<a href="https://msdn.microsoft.com/0183584f-105e-4fa3-8991-d3f2dfca1d62">HttpSendHttpResponse</a>



<a href="https://msdn.microsoft.com/f2ff2e40-ef1f-4c35-a615-f31ac63ab738">HttpSendResponseEntityBody</a>
 

 

