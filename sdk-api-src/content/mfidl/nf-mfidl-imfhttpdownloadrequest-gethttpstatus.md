---
UID: NF:mfidl.IMFHttpDownloadRequest.GetHttpStatus
title: IMFHttpDownloadRequest::GetHttpStatus
author: windows-sdk-content
description: Invoked by Microsoft Media Foundation to retrieve the HTTP status code that the server specified in its response. Media Foundation invokes this method after a successful call to EndReceiveResponse.
old-location: mf\imfhttpdownloadrequest_gethttpstatus.htm
old-project: medfound
ms.assetid: E084CF25-BEFA-4061-AA77-2CFC57CF6DCE
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetHttpStatus, GetHttpStatus method [Media Foundation], GetHttpStatus method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],GetHttpStatus method, IMFHttpDownloadRequest.GetHttpStatus, IMFHttpDownloadRequest::GetHttpStatus, mf.imfhttpdownloadrequest_gethttpstatus, mfidl/IMFHttpDownloadRequest::GetHttpStatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
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
 - IMFHttpDownloadRequest.GetHttpStatus
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFHttpDownloadRequest::GetHttpStatus


## -description


Invoked by Microsoft Media Foundation to retrieve the HTTP status code that the server specified in its response. Media Foundation invokes this method after a successful call to <a href="https://msdn.microsoft.com/FC342FB9-930F-4EA7-9057-51AF10D13ED9">EndReceiveResponse</a>.


## -parameters




### -param pdwHttpStatus [out]

The HTTP status code of the response. For example, the value is  200 for a typical successful response.


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
Successfully returned the HTTP status code.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The HTTP response has not yet been received.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">

                The <i>pdwHttpStatus</i> parameter is an invalid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a>
 

 

