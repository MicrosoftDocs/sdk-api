---
UID: NF:mfidl.IMFHttpDownloadRequest.EndReadPayload
title: IMFHttpDownloadRequest::EndReadPayload
author: windows-sdk-content
description: Invoked by Microsoft Media Foundation to complete the asynchronous operation started by BeginReadPayload.
old-location: mf\imfhttpdownloadrequest_endreadpayload.htm
tech.root: medfound
ms.assetid: 491437FE-1401-4841-AE0E-428F28E34D4D
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: EndReadPayload, EndReadPayload method [Media Foundation], EndReadPayload method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],EndReadPayload method, IMFHttpDownloadRequest.EndReadPayload, IMFHttpDownloadRequest::EndReadPayload, mf.imfhttpdownloadrequest_endreadpayload, mfidl/IMFHttpDownloadRequest::EndReadPayload
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
 - IMFHttpDownloadRequest.EndReadPayload
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFHttpDownloadRequest::EndReadPayload


## -description


Invoked by Microsoft Media Foundation to complete the asynchronous operation started by <a href="https://msdn.microsoft.com/01B799C2-63C6-4BDC-AAE2-CFC3C426A218">BeginReadPayload</a>. When this method completes successfully, the payload data will have been written to the buffer that Media Foundation provided when invoking <b>BeginReadPayload</b>.


## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Microsoft Media Foundation will pass in the same pointer that its callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.


### -param pqwOffset [out]

The offset of the first byte written to the buffer, relative to the complete message body of the current HTTP request. For example, when Media Foundation invokes <a href="https://msdn.microsoft.com/01B799C2-63C6-4BDC-AAE2-CFC3C426A218">BeginReadPayload</a> for the first time on a given <a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a>, and specifies a buffer size of 100, the <i>pqwOffset</i> parameter will be set to 0. Then, when Media Foundation invokes <b>BeginReadPayload</b> for the second time on the same <b>IMNFHttpDownloadRequest</b>, the <i>pqwOffset</i> parameter will be set to 100.


### -param pcbRead [out]

Specifies the number of bytes written to the buffer that Media Foundation provided when invoking <a href="https://msdn.microsoft.com/01B799C2-63C6-4BDC-AAE2-CFC3C426A218">BeginReadPayload</a>. Note that this value must always be equal to the size of the buffer specified in <b>BeginReadPayload</b>, unless the request failed, or unless the end of the message body has been reached.


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
Successfully wrote data to the buffer provided in <a href="https://msdn.microsoft.com/01B799C2-63C6-4BDC-AAE2-CFC3C426A218">BeginReadPayload</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a>
 

 

