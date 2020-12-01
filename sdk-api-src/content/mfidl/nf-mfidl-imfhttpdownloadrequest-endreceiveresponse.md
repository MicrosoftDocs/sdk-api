---
UID: NF:mfidl.IMFHttpDownloadRequest.EndReceiveResponse
title: IMFHttpDownloadRequest::EndReceiveResponse (mfidl.h)
description: Invoked by Microsoft Media Foundation to complete the asynchronous operation started by BeginReceiveResponse.
helpviewer_keywords: ["EndReceiveResponse","EndReceiveResponse method [Media Foundation]","EndReceiveResponse method [Media Foundation]","IMFHttpDownloadRequest interface","IMFHttpDownloadRequest interface [Media Foundation]","EndReceiveResponse method","IMFHttpDownloadRequest.EndReceiveResponse","IMFHttpDownloadRequest::EndReceiveResponse","mf.imfhttpdownloadrequest_endreceiveresponse","mfidl/IMFHttpDownloadRequest::EndReceiveResponse"]
old-location: mf\imfhttpdownloadrequest_endreceiveresponse.htm
tech.root: mf
ms.assetid: FC342FB9-930F-4EA7-9057-51AF10D13ED9
ms.date: 12/05/2018
ms.keywords: EndReceiveResponse, EndReceiveResponse method [Media Foundation], EndReceiveResponse method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],EndReceiveResponse method, IMFHttpDownloadRequest.EndReceiveResponse, IMFHttpDownloadRequest::EndReceiveResponse, mf.imfhttpdownloadrequest_endreceiveresponse, mfidl/IMFHttpDownloadRequest::EndReceiveResponse
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
 - IMFHttpDownloadRequest::EndReceiveResponse
 - mfidl/IMFHttpDownloadRequest::EndReceiveResponse
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
 - IMFHttpDownloadRequest.EndReceiveResponse
---

# IMFHttpDownloadRequest::EndReceiveResponse


## -description

Invoked by Microsoft Media Foundation to complete the asynchronous operation started by <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-beginreceiveresponse">BeginReceiveResponse</a>.

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
Successfully received the HTTP response and associated headers.

</td>
</tr>
</table>

## -remarks

If the server failed the request but responded with a specific HTTP status code, the <b>EndReceiveResponse</b> should still return S_OK. Media Foundation will invoke the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-gethttpstatus">GetHttpStatus</a> method to retrieve the HTTP status code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a>