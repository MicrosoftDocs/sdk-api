---
UID: NF:mfidl.IMFHttpDownloadRequest.EndReceiveResponse
title: IMFHttpDownloadRequest::EndReceiveResponse
author: windows-sdk-content
description: Invoked by Microsoft Media Foundation to complete the asynchronous operation started by BeginReceiveResponse.
old-location: mf\imfhttpdownloadrequest_endreceiveresponse.htm
tech.root: MedFound
ms.assetid: FC342FB9-930F-4EA7-9057-51AF10D13ED9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: EndReceiveResponse, EndReceiveResponse method [Media Foundation], EndReceiveResponse method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],EndReceiveResponse method, IMFHttpDownloadRequest.EndReceiveResponse, IMFHttpDownloadRequest::EndReceiveResponse, mf.imfhttpdownloadrequest_endreceiveresponse, mfidl/IMFHttpDownloadRequest::EndReceiveResponse
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
 - IMFHttpDownloadRequest.EndReceiveResponse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFHttpDownloadRequest::EndReceiveResponse


## -description


Invoked by Microsoft Media Foundation to complete the asynchronous operation started by <a href="https://msdn.microsoft.com/6D5DB091-426B-4E89-8657-0BDC6427B23A">BeginReceiveResponse</a>.


## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Microsoft Media Foundation will pass in the same pointer that its callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.


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



If the server failed the request but responded with a specific HTTP status code, the <b>EndReceiveResponse</b> should still return S_OK. Media Foundation will invoke the <a href="https://msdn.microsoft.com/E084CF25-BEFA-4061-AA77-2CFC57CF6DCE">GetHttpStatus</a> method to retrieve the HTTP status code.




## -see-also




<a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a>
 

 

