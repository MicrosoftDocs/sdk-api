---
UID: NF:mfidl.IMFHttpDownloadRequest.BeginReadPayload
title: IMFHttpDownloadRequest::BeginReadPayload (mfidl.h)
description: Invoked by Microsoft Media Foundation to receive the message body of the response to a previously sent HTTP or HTTPS request.
helpviewer_keywords: ["BeginReadPayload","BeginReadPayload method [Media Foundation]","BeginReadPayload method [Media Foundation]","IMFHttpDownloadRequest interface","IMFHttpDownloadRequest interface [Media Foundation]","BeginReadPayload method","IMFHttpDownloadRequest.BeginReadPayload","IMFHttpDownloadRequest::BeginReadPayload","mf.imfhttpdownloadrequest_beginreadpayload","mfidl/IMFHttpDownloadRequest::BeginReadPayload"]
old-location: mf\imfhttpdownloadrequest_beginreadpayload.htm
tech.root: mf
ms.assetid: 01B799C2-63C6-4BDC-AAE2-CFC3C426A218
ms.date: 12/05/2018
ms.keywords: BeginReadPayload, BeginReadPayload method [Media Foundation], BeginReadPayload method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],BeginReadPayload method, IMFHttpDownloadRequest.BeginReadPayload, IMFHttpDownloadRequest::BeginReadPayload, mf.imfhttpdownloadrequest_beginreadpayload, mfidl/IMFHttpDownloadRequest::BeginReadPayload
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
 - IMFHttpDownloadRequest::BeginReadPayload
 - mfidl/IMFHttpDownloadRequest::BeginReadPayload
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
 - IMFHttpDownloadRequest.BeginReadPayload
---

# IMFHttpDownloadRequest::BeginReadPayload


## -description

Invoked by Microsoft Media Foundation to receive the message body of the response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endreceiveresponse">EndReceiveResponse</a> method. Since the size of the message body may be large, or unknown, Media Foundation may invoke this method multiple times to retrieve the message body in piecemeal fashion.

## -parameters

### -param pb [out]

Pointer to a buffer that receives the data.

### -param cb [in]

Specifies the size of the <i>pb</i> buffer, in bytes.

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

## -remarks

Microsoft Media Foundation never invokes <b>BeginReadPayload</b> while a previous call to <b>BeginReadPayload</b> has not yet completed.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a>