---
UID: NF:http.HttpReceiveClientCertificate
title: HttpReceiveClientCertificate function
author: windows-sdk-content
description: The HttpReceiveClientCertificate function is used by a server application to retrieve a client SSL certificate or channel binding token (CBT).
old-location: http\httpreceiveclientcertificate.htm
tech.root: http
ms.assetid: f0cf7b77-2868-4142-a663-32d6ea7df9e9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HTTP_RECEIVE_SECURE_CHANNEL_TOKEN, HttpReceiveClientCertificate, HttpReceiveClientCertificate function [HTTP], _http_httpreceiveclientcertificate, http.httpreceiveclientcertificate, http/HttpReceiveClientCertificate
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
 - HttpReceiveClientCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HttpReceiveClientCertificate function


## -description


The 
<b>HttpReceiveClientCertificate</b> function is used by a server application to retrieve a client SSL certificate or channel binding token (CBT).


## -parameters




### -param RequestQueueHandle [in]

A handle to the request queue with which the specified SSL client or CBT is associated. A request queue is created and its handle returned by a call to the 
<a href="https://msdn.microsoft.com/a0f4112e-db81-4eda-afeb-d00117f7240c">HttpCreateRequestQueue</a> function.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>The handle to the request queue is created by the <a href="https://msdn.microsoft.com/c3741092-c23a-465f-9a65-5bcbf977fad3">HttpCreateHttpHandle</a> function.


### -param ConnectionId [in]

A value that identifies the connection to the client. This value is obtained from the <b>ConnectionId</b> element of an 
<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a> structure filled in by the 
<a href="https://msdn.microsoft.com/ad9e80f7-04c4-4108-a7ab-40eb57d00e3b">HttpReceiveHttpRequest</a> function.


### -param Flags [in]

A value that modifies the behavior of the <b>HttpReceiveClientCertificate</b> function

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_RECEIVE_SECURE_CHANNEL_TOKEN"></a><a id="http_receive_secure_channel_token"></a><dl>
<dt><b>HTTP_RECEIVE_SECURE_CHANNEL_TOKEN</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The <i>pSslClientCertInfo</i> parameter will be populated with CBT data.

This value is supported on Windows 7, Windows Server 2008 R2, and later. 

</td>
</tr>
</table>
 


### -param SslClientCertInfo [out]

If the <i>Flags</i> parameter is 0, then this parameter points to an 
<a href="https://msdn.microsoft.com/bfe6a9a9-6117-4403-a83f-e9448615500b">HTTP_SSL_CLIENT_CERT_INFO</a> structure into which the function writes the requested client certificate information. The buffer pointed to by the <i>pSslClientCertInfo</i> should be sufficiently large enough to hold the <b>HTTP_SSL_CLIENT_CERT_INFO</b> structure plus the value of the <b>CertEncodedSize</b> member of this structure.

If the <i>Flags</i> parameter is <b>HTTP_RECEIVE_SECURE_CHANNEL_TOKEN</b>, then this parameter points to an 
<a href="https://msdn.microsoft.com/70f52486-2632-4e15-998b-4d87a86cb11f">HTTP_REQUEST_CHANNEL_BIND_STATUS</a> structure into which the function writes the requested CBT information. The buffer pointed to by the <i>pSslClientCertInfo</i> should be sufficiently large enough to hold the <b>HTTP_REQUEST_CHANNEL_BIND_STATUS</b>  structure plus the value of the <b>ChannelTokenSize</b> member of this structure.


### -param SslClientCertInfoSize [in]

The size, in bytes, of the buffer pointed to by the <i>pSslClientCertInfo</i> parameter.


### -param BytesReceived [out, optional]

An optional pointer to a variable that receives  the number of bytes to be written to the structure pointed to by <i>pSslClientCertInfo</i>. If not used, set it to <b>NULL</b>. 




When making an asynchronous call using <i>pOverlapped</i>, set <i>pBytesReceived</i> to <b>NULL</b>. Otherwise, when <i>pOverlapped</i> is set to <b>NULL</b>, <i>pBytesReceived</i> must contain a valid memory address, and not be set to <b>NULL</b>.


### -param Overlapped

TBD




#### - pOverlapped [in, optional]

For asynchronous calls, set <i>pOverlapped</i> to point to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure, or for synchronous calls, set it to <b>NULL</b>. 




A synchronous call blocks until the client certificate is retrieved, whereas an asynchronous call immediately returns <b>ERROR_IO_PENDING</b> and the calling application then uses 
<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> or I/O completion ports to determine when the operation is completed. For more information about using 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structures for synchronization, see the section 
<a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded. 

All the data has been written into the buffer pointed to by the <i>pSslClientCertInfo</i> parameter. The  <i>NumberOfBytesTransferred</i> indicates how many bytes were written into the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The function is being used asynchronously. The operation has been initiated and will complete later through normal overlapped I/O completion mechanisms.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the supplied parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>pSslClientCertInfo</i> parameter is too small to receive the data and no data was written.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>pSslClientCertInfo</i> parameter is not large enough to receive all the data. Only the basic structure has been written and only partially populated.

When the <i>Flags</i> parameter is 0, the <a href="https://msdn.microsoft.com/bfe6a9a9-6117-4403-a83f-e9448615500b">HTTP_SSL_CLIENT_CERT_INFO</a>structure has been written with the <b>CertEncodedSize</b> member populated. The caller should call the function again with a buffer that is at least the size, in bytes, of  the <b>HTTP_SSL_CLIENT_CERT_INFO</b> structure plus the value of the <b>CertEncodedSize</b> member.

When the <i>Flags</i> parameter is <b>HTTP_RECEIVE_SECURE_CHANNEL_TOKEN</b>, the <a href="https://msdn.microsoft.com/70f52486-2632-4e15-998b-4d87a86cb11f">HTTP_REQUEST_CHANNEL_BIND_STATUS</a>  structure has been written with the <b>ChannelTokenSize</b> member populated. The caller should call the function again with a buffer that is at least the size, in bytes, of the <b>HTTP_REQUEST_CHANNEL_BIND_STATUS</b>  plus  the value of the <b>ChannelTokenSize</b> member.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The function cannot find the client certificate or CBT.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
A <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in the <i>WinError.h</i> header file.

</td>
</tr>
</table>
 




## -remarks



The behavior of the <b>HttpReceiveClientCertificate</b> function varies based on whether an client SSL certificate or a channel binding token is requested.

In the case of a synchronous call to the <b>HttpReceiveClientCertificate</b> function , the number of bytes received is returned in the value pointed to by the <i>pBytesReceived</i> parameter.

In the case of an asynchronous call to the <b>HttpReceiveClientCertificate</b> function, the number of bytes received is returned by the standard mechanisms used for asynchronous calls. The  <i>lpNumberOfBytesTransferred</i> parameter returned by the 
<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> function contains the number of bytes received.




## -see-also




<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/1da9907d-a09d-41e1-aca1-9a8e2b91296f">HTTP Server API Version 1.0 Functions</a>



<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a>



<a href="https://msdn.microsoft.com/70f52486-2632-4e15-998b-4d87a86cb11f">HTTP_REQUEST_CHANNEL_BIND_STATUS</a>



<a href="https://msdn.microsoft.com/bfe6a9a9-6117-4403-a83f-e9448615500b">HTTP_SSL_CLIENT_CERT_INFO</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>
 

 

