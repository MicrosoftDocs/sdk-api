---
UID: NF:mfidl.IMFHttpDownloadRequest.BeginReceiveResponse
title: IMFHttpDownloadRequest::BeginReceiveResponse (mfidl.h)
description: Invoked by Microsoft Media Foundation to receive the response, provided by the server, in response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the EndSendRequest method.
helpviewer_keywords: ["BeginReceiveResponse","BeginReceiveResponse method [Media Foundation]","BeginReceiveResponse method [Media Foundation]","IMFHttpDownloadRequest interface","IMFHttpDownloadRequest interface [Media Foundation]","BeginReceiveResponse method","IMFHttpDownloadRequest.BeginReceiveResponse","IMFHttpDownloadRequest::BeginReceiveResponse","mf.imfhttpdownloadrequest_beginreceiveresponse","mfidl/IMFHttpDownloadRequest::BeginReceiveResponse"]
old-location: mf\imfhttpdownloadrequest_beginreceiveresponse.htm
tech.root: mf
ms.assetid: 6D5DB091-426B-4E89-8657-0BDC6427B23A
ms.date: 12/05/2018
ms.keywords: BeginReceiveResponse, BeginReceiveResponse method [Media Foundation], BeginReceiveResponse method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],BeginReceiveResponse method, IMFHttpDownloadRequest.BeginReceiveResponse, IMFHttpDownloadRequest::BeginReceiveResponse, mf.imfhttpdownloadrequest_beginreceiveresponse, mfidl/IMFHttpDownloadRequest::BeginReceiveResponse
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
 - IMFHttpDownloadRequest::BeginReceiveResponse
 - mfidl/IMFHttpDownloadRequest::BeginReceiveResponse
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
 - IMFHttpDownloadRequest.BeginReceiveResponse
---

# IMFHttpDownloadRequest::BeginReceiveResponse


## -description

Invoked by Microsoft Media Foundation to receive the response, provided by the server, in response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endsendrequest">EndSendRequest</a> method.

## -parameters

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
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a>