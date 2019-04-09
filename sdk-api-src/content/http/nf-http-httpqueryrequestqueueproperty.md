---
UID: NF:http.HttpQueryRequestQueueProperty
title: HttpQueryRequestQueueProperty function (http.h)
author: windows-sdk-content
description: Queries a property of the request queue identified by the specified handle.
old-location: http\httpqueryrequestqueueproperty.htm
tech.root: http
ms.assetid: a3b1e85e-f152-4038-a56a-3d5985757c45
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HttpQueryRequestQueueProperty, HttpQueryRequestQueueProperty function [HTTP], HttpServer503VerbosityProperty, HttpServerQueueLengthProperty, HttpServerStateProperty, http.httpqueryrequestqueueproperty, http/HttpQueryRequestQueueProperty
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpQueryRequestQueueProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HttpQueryRequestQueueProperty function


## -description


The <b>HttpQueryRequestQueueProperty</b> function queries a property of the request queue identified by the specified handle.


## -parameters




### -param RequestQueueProperty [in]

The handle to the request queue for which the property setting is returned. A request queue is created and its handle returned by a call to the 
<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> function.


### -param Property [in]

A member of the  <a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HTTP_SERVER_PROPERTY</a> enumeration that describes the property type that is set. This can be one of the following:

<table>
<tr>
<th>Property</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HttpServer503VerbosityProperty"></a><a id="httpserver503verbosityproperty"></a><a id="HTTPSERVER503VERBOSITYPROPERTY"></a><dl>
<dt><b>HttpServer503VerbosityProperty</b></dt>
</dl>
</td>
<td width="60%">
Queries the current verbosity level of 503 responses generated for the requests queue.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerQueueLengthProperty"></a><a id="httpserverqueuelengthproperty"></a><a id="HTTPSERVERQUEUELENGTHPROPERTY"></a><dl>
<dt><b>HttpServerQueueLengthProperty</b></dt>
</dl>
</td>
<td width="60%">
Queries the limit on the number of outstanding requests in the request queue.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerStateProperty"></a><a id="httpserverstateproperty"></a><a id="HTTPSERVERSTATEPROPERTY"></a><dl>
<dt><b>HttpServerStateProperty</b></dt>
</dl>
</td>
<td width="60%">
Queries the current state of the request queue. The state must be either active or inactive.

</td>
</tr>
</table>
 


### -param PropertyInformation [out]

A pointer to the buffer that receives the property information.

<i>pPropertyInformation</i> points to one of the following property information values based on the property that is set.<table>
<tr>
<th>Property</th>
<th>Value</th>
</tr>
<tr>
<td>HttpServerStateProperty</td>
<td>
<a href="https://msdn.microsoft.com/15e27788-2d1a-4818-b31f-2faf649e15b2">HTTP_ENABLED_STATE</a> (enumeration member)</td>
</tr>
<tr>
<td>HttpServerQueueLengthProperty</td>
<td>ULONG</td>
</tr>
<tr>
<td>HttpServer503VerbosityProperty</td>
<td>
<a href="https://msdn.microsoft.com/e103bdf4-dc48-45ba-84dc-4161310ee3ff">HTTP_503_RESPONSE_VERBOSITY</a> (enumeration member)</td>
</tr>
</table>
 




### -param PropertyInformationLength [in]

The length, in bytes, of the buffer pointed to by the <i>pPropertyInformation</i> parameter.


### -param Reserved1 [in]

Reserved. Must be zero.


### -param ReturnLength [out, optional]

The number, in bytes, returned in the  <i>pPropertyInformation</i> buffer if not <b>NULL</b>.

If the output buffer is too small, the call fails with a return value of <b>ERROR_MORE_DATA</b>. The value pointed to by <i>pReturnLength</i> can be used to determine the minimum length of the buffer required for the call to succeed.


### -param Reserved2 [in]

This parameter is reserved and must be <b>NULL</b>.


## -returns



If the function succeeds, it returns <b>NO_ERROR</b>.

If the function fails, it returns one of the following error codes.

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
The <i>Reserved</i> parameter is not zero or the  <i>pReserved</i> parameter is not <b>NULL</b>.

The property type specified in the <i>Property</i> parameter is not supported on request queues.

The <i>pPropertyInformation</i> parameter is <b>NULL</b>.

The  <i>PropertyInformationLength</i> parameter is zero.

The application does not have permission to open the request queue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The size, in bytes, of the buffer pointed to by the  <i>pPropertyInformation</i> parameter is too small to receive the property information. Call the function again with a buffer at least as large as the size pointed to by <i>pReturnLength</i> on exit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The handle to the request queue is an HTTP version 1.0 handle. Property management is only supported for HTTP version 2.0 and later request queues.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/dfbc2d32-c1f6-41b1-8f4f-9e5e9f6dd9e1">HttpCloseRequestQueue</a>



<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a>



<a href="https://msdn.microsoft.com/56111cc0-94c8-47dc-a3bb-ffc5dae772fe">HttpSetRequestQueueProperty</a>



<a href="https://msdn.microsoft.com/f6640565-a5a1-4a71-938c-1adf54beb40a">HttpShutdownRequestQueue</a>
 

 

