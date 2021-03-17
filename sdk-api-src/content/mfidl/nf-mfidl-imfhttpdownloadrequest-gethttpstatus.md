---
UID: NF:mfidl.IMFHttpDownloadRequest.GetHttpStatus
title: IMFHttpDownloadRequest::GetHttpStatus (mfidl.h)
description: Invoked by Microsoft Media Foundation to retrieve the HTTP status code that the server specified in its response. Media Foundation invokes this method after a successful call to EndReceiveResponse.
helpviewer_keywords: ["GetHttpStatus","GetHttpStatus method [Media Foundation]","GetHttpStatus method [Media Foundation]","IMFHttpDownloadRequest interface","IMFHttpDownloadRequest interface [Media Foundation]","GetHttpStatus method","IMFHttpDownloadRequest.GetHttpStatus","IMFHttpDownloadRequest::GetHttpStatus","mf.imfhttpdownloadrequest_gethttpstatus","mfidl/IMFHttpDownloadRequest::GetHttpStatus"]
old-location: mf\imfhttpdownloadrequest_gethttpstatus.htm
tech.root: mf
ms.assetid: E084CF25-BEFA-4061-AA77-2CFC57CF6DCE
ms.date: 12/05/2018
ms.keywords: GetHttpStatus, GetHttpStatus method [Media Foundation], GetHttpStatus method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],GetHttpStatus method, IMFHttpDownloadRequest.GetHttpStatus, IMFHttpDownloadRequest::GetHttpStatus, mf.imfhttpdownloadrequest_gethttpstatus, mfidl/IMFHttpDownloadRequest::GetHttpStatus
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
 - IMFHttpDownloadRequest::GetHttpStatus
 - mfidl/IMFHttpDownloadRequest::GetHttpStatus
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
 - IMFHttpDownloadRequest.GetHttpStatus
---

# IMFHttpDownloadRequest::GetHttpStatus


## -description

Invoked by Microsoft Media Foundation to retrieve the HTTP status code that the server specified in its response. Media Foundation invokes this method after a successful call to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endreceiveresponse">EndReceiveResponse</a>.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a>