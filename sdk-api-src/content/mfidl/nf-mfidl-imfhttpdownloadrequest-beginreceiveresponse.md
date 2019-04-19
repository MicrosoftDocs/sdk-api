---
UID: NF:mfidl.IMFHttpDownloadRequest.BeginReceiveResponse
title: IMFHttpDownloadRequest::BeginReceiveResponse (mfidl.h)
author: windows-sdk-content
description: Invoked by Microsoft Media Foundation to receive the response, provided by the server, in response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the EndSendRequest method.
old-location: mf\imfhttpdownloadrequest_beginreceiveresponse.htm
tech.root: medfound
ms.assetid: 6D5DB091-426B-4E89-8657-0BDC6427B23A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BeginReceiveResponse, BeginReceiveResponse method [Media Foundation], BeginReceiveResponse method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],BeginReceiveResponse method, IMFHttpDownloadRequest.BeginReceiveResponse, IMFHttpDownloadRequest::BeginReceiveResponse, mf.imfhttpdownloadrequest_beginreceiveresponse, mfidl/IMFHttpDownloadRequest::BeginReceiveResponse
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
 - IMFHttpDownloadRequest.BeginReceiveResponse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFHttpDownloadRequest::BeginReceiveResponse


## -description


Invoked by Microsoft Media Foundation to receive the response, provided by the server, in response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the <a href="https://msdn.microsoft.com/2B1554C7-2814-4A9E-BBAC-B25C78775420">EndSendRequest</a> method.


## -parameters




### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object that is implemented by Microsoft Media Foundation.


### -param punkState

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of a state object, defined by Microsoft Media Foundation. This parameter can be NULL.


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




<a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a>
 

 

