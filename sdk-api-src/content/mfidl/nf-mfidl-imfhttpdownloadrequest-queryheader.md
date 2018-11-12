---
UID: NF:mfidl.IMFHttpDownloadRequest.QueryHeader
title: IMFHttpDownloadRequest::QueryHeader
author: windows-sdk-content
description: Invoked by Microsoft Media Foundation to retrieve the values of specified HTTP headers from the response to a previously sent HTTP or HTTPS request.
old-location: mf\imfhttpdownloadrequest_queryheader.htm
tech.root: medfound
ms.assetid: BFAE5257-0BE8-47F3-B3CD-490885E60065
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFHttpDownloadRequest interface [Media Foundation],QueryHeader method, IMFHttpDownloadRequest.QueryHeader, IMFHttpDownloadRequest::QueryHeader, QueryHeader, QueryHeader method [Media Foundation], QueryHeader method [Media Foundation],IMFHttpDownloadRequest interface, mf.imfhttpdownloadrequest_queryheader, mfidl/IMFHttpDownloadRequest::QueryHeader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFHttpDownloadRequest.QueryHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFHttpDownloadRequest::QueryHeader


## -description


Invoked by Microsoft Media Foundation to retrieve the values of specified HTTP headers from the response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the <a href="https://msdn.microsoft.com/FC342FB9-930F-4EA7-9057-51AF10D13ED9">EndReceiveResponse</a> method.


## -parameters




### -param szHeaderName [in]

The name of the HTTP header for which the value is being queried.


### -param dwIndex [in]

The index number of the specified header, for the case where the response contains multiple headers with the same name. A value of 0 indicates that the value of the first header with the specified name is requested, 1 indicates that the second header is requested, and so on.


### -param ppszHeaderValue [out]

Set to the value of the requested header, not including the carriage return or line feed characters. The memory for <i>ppszHeaderValue</i> must be allocated with <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and will be freed by Media Foundation with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully returned the value of the specified header with the specified index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppszHeaderValue</i> parameter is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_OUT_OF_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwIndex</i> parameter value is out of range.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a>
 

 

