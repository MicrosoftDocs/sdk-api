---
UID: NF:mfidl.IMFHttpDownloadRequest.EndSendRequest
title: IMFHttpDownloadRequest::EndSendRequest (mfidl.h)
description: Invoked by Microsoft Media Foundation to complete the asynchronous operation started by BeginSendRequest.
helpviewer_keywords: ["EndSendRequest","EndSendRequest method [Media Foundation]","EndSendRequest method [Media Foundation]","IMFHttpDownloadRequest interface","IMFHttpDownloadRequest interface [Media Foundation]","EndSendRequest method","IMFHttpDownloadRequest.EndSendRequest","IMFHttpDownloadRequest::EndSendRequest","mf.imfhttpdownloadrequest_endsendrequest","mfidl/IMFHttpDownloadRequest::EndSendRequest"]
old-location: mf\imfhttpdownloadrequest_endsendrequest.htm
tech.root: mf
ms.assetid: 2B1554C7-2814-4A9E-BBAC-B25C78775420
ms.date: 12/05/2018
ms.keywords: EndSendRequest, EndSendRequest method [Media Foundation], EndSendRequest method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],EndSendRequest method, IMFHttpDownloadRequest.EndSendRequest, IMFHttpDownloadRequest::EndSendRequest, mf.imfhttpdownloadrequest_endsendrequest, mfidl/IMFHttpDownloadRequest::EndSendRequest
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
 - IMFHttpDownloadRequest::EndSendRequest
 - mfidl/IMFHttpDownloadRequest::EndSendRequest
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
 - IMFHttpDownloadRequest.EndSendRequest
---

# IMFHttpDownloadRequest::EndSendRequest


## -description

Invoked by Microsoft Media Foundation to complete the asynchronous operation started by <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-beginsendrequest">BeginSendRequest</a>.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Microsoft Media Foundation will pass in the same pointer that its callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

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
The request was successfully sent to the server.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a>