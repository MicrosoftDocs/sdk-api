---
UID: NF:mfidl.IMFHttpDownloadRequest.HasNullSourceOrigin
title: IMFHttpDownloadRequest::HasNullSourceOrigin
author: windows-sdk-content
description: Invoked by Microsoft Media Foundation to detect the case when a HTTP or HTTPS request has been redirected to a different server of different &#0034;origin&#0034;.
old-location: mf\imfhttpdownloadrequest_hasnullsourceorigin.htm
tech.root: medfound
ms.assetid: D83F079F-605A-4F62-B037-3C5D0487D778
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: HasNullSourceOrigin, HasNullSourceOrigin method [Media Foundation], HasNullSourceOrigin method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],HasNullSourceOrigin method, IMFHttpDownloadRequest.HasNullSourceOrigin, IMFHttpDownloadRequest::HasNullSourceOrigin, mf.imfhttpdownloadrequest_hasnullsourceorigin, mfidl/IMFHttpDownloadRequest::HasNullSourceOrigin
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
 - IMFHttpDownloadRequest.HasNullSourceOrigin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFHttpDownloadRequest.HasNullSourceOrigin
: 
---

# IMFHttpDownloadRequest::HasNullSourceOrigin


## -description


Invoked by Microsoft Media Foundation to detect the case when a HTTP or HTTPS request has been redirected to a different server of different "origin". 


## -parameters




### -param pfNullSourceOrigin [out]

Set to TRUE if the current request has a “null” source origin. The source origin would become “null” if the HTTP request was redirected from one server to another, and the two servers have different origins.


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
Successfully completed the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfNullSOurceOrigin</i> parameter is an invalid pointer.

</td>
</tr>
</table>
 




## -remarks



The <i>pfNullSourceOrigin</i> parameter should be set to TRUE if <b>HasNullSourceOrigin</b> is invoked before <a href="https://msdn.microsoft.com/FC342FB9-930F-4EA7-9057-51AF10D13ED9">EndReceiveResponse</a> has been invoked. For more information about the concept of origin in HTTP, see <a href="https://tools.ietf.org/html/rfc6454">RFC-6454</a>.




## -see-also




<a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a>
 

 

