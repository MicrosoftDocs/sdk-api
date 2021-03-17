---
UID: NF:mfidl.IMFHttpDownloadRequest.BeginSendRequest
title: IMFHttpDownloadRequest::BeginSendRequest (mfidl.h)
description: Invoked by Microsoft Media Foundation to send a HTTP or HTTPS request.
helpviewer_keywords: ["BeginSendRequest","BeginSendRequest method [Media Foundation]","BeginSendRequest method [Media Foundation]","IMFHttpDownloadRequest interface","IMFHttpDownloadRequest interface [Media Foundation]","BeginSendRequest method","IMFHttpDownloadRequest.BeginSendRequest","IMFHttpDownloadRequest::BeginSendRequest","mf.imfhttpdownloadrequest_beginsendrequest","mfidl/IMFHttpDownloadRequest::BeginSendRequest"]
old-location: mf\imfhttpdownloadrequest_beginsendrequest.htm
tech.root: mf
ms.assetid: 38025B19-146A-4050-9BD2-2CF974729FE3
ms.date: 12/05/2018
ms.keywords: BeginSendRequest, BeginSendRequest method [Media Foundation], BeginSendRequest method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],BeginSendRequest method, IMFHttpDownloadRequest.BeginSendRequest, IMFHttpDownloadRequest::BeginSendRequest, mf.imfhttpdownloadrequest_beginsendrequest, mfidl/IMFHttpDownloadRequest::BeginSendRequest
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
 - IMFHttpDownloadRequest::BeginSendRequest
 - mfidl/IMFHttpDownloadRequest::BeginSendRequest
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
 - IMFHttpDownloadRequest.BeginSendRequest
---

# IMFHttpDownloadRequest::BeginSendRequest


## -description

Invoked by Microsoft Media Foundation to send a HTTP or HTTPS request

## -parameters

### -param pbPayload [in]

Pointer to a buffer that contains the message payload to send in the request. This parameter is used for POST requests. GET requests do not carry a message payload and therefore <i>pbPayload</i> is NULL.

### -param cbPayload [in]

The size of the <i>pbPayload</i> buffer, in bytes.

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object that is implemented by Microsoft Media Foundation.

### -param punkState

Pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of a state object, defined by Microsoft Media Foundation. This parameter can be NULL.

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
Successfully started the asynchronous operation.

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
</table>

## -remarks

The implementation of <b>BeginWrite</b> does not need to make a private copy of the memory pointed to by <i>pbPayload</i>, as Microsoft Media Foundation will not reallocate, free, or write to the buffer while an asynchronous write is still pending.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a>