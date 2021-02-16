---
UID: NF:mfidl.IMFHttpDownloadRequest.HasNullSourceOrigin
title: IMFHttpDownloadRequest::HasNullSourceOrigin (mfidl.h)
description: Invoked by Microsoft Media Foundation to detect the case when a HTTP or HTTPS request has been redirected to a different server of different &quot;origin&quot;.
helpviewer_keywords: ["HasNullSourceOrigin","HasNullSourceOrigin method [Media Foundation]","HasNullSourceOrigin method [Media Foundation]","IMFHttpDownloadRequest interface","IMFHttpDownloadRequest interface [Media Foundation]","HasNullSourceOrigin method","IMFHttpDownloadRequest.HasNullSourceOrigin","IMFHttpDownloadRequest::HasNullSourceOrigin","mf.imfhttpdownloadrequest_hasnullsourceorigin","mfidl/IMFHttpDownloadRequest::HasNullSourceOrigin"]
old-location: mf\imfhttpdownloadrequest_hasnullsourceorigin.htm
tech.root: mf
ms.assetid: D83F079F-605A-4F62-B037-3C5D0487D778
ms.date: 12/05/2018
ms.keywords: HasNullSourceOrigin, HasNullSourceOrigin method [Media Foundation], HasNullSourceOrigin method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],HasNullSourceOrigin method, IMFHttpDownloadRequest.HasNullSourceOrigin, IMFHttpDownloadRequest::HasNullSourceOrigin, mf.imfhttpdownloadrequest_hasnullsourceorigin, mfidl/IMFHttpDownloadRequest::HasNullSourceOrigin
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFHttpDownloadRequest::HasNullSourceOrigin
 - mfidl/IMFHttpDownloadRequest::HasNullSourceOrigin
dev_langs:
 - c++
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

The <i>pfNullSourceOrigin</i> parameter should be set to TRUE if <b>HasNullSourceOrigin</b> is invoked before <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endreceiveresponse">EndReceiveResponse</a> has been invoked. For more information about the concept of origin in HTTP, see <a href="https://tools.ietf.org/html/rfc6454">RFC-6454</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a>