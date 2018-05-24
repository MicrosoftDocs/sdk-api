---
UID: NF:mfidl.IMFHttpDownloadRequest.GetAtEndOfPayload
title: IMFHttpDownloadRequest::GetAtEndOfPayload
author: windows-driver-content
description: Invoked by Microsoft Media Foundation to check if it should invoke BeginReadPayload to read data from the message body of the response.
old-location: mf\imfhttpdownloadrequest_getatendofpayload.htm
old-project: medfound
ms.assetid: 2F2D65BA-4719-4633-9B2D-2CAF88F4E3DD
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetAtEndOfPayload, GetAtEndOfPayload method [Media Foundation], GetAtEndOfPayload method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],GetAtEndOfPayload method, IMFHttpDownloadRequest.GetAtEndOfPayload, IMFHttpDownloadRequest::GetAtEndOfPayload, mf.imfhttpdownloadrequest_getatendofpayload, mfidl/IMFHttpDownloadRequest::GetAtEndOfPayload
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplat.lib
-	mfplat.dll
-	mfplat.dll
-	mfplat.dll.dll
api_name:
-	IMFHttpDownloadRequest.GetAtEndOfPayload
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFHttpDownloadRequest::GetAtEndOfPayload


## -description


Invoked by Microsoft Media Foundation to check if it should invoke <a href="https://msdn.microsoft.com/01B799C2-63C6-4BDC-AAE2-CFC3C426A218">BeginReadPayload</a> to read data from the message body of the response. During the processing of a typical HTTP response, Media Foundation will invoke <b>BeginReadPayload</b> multiple times, but once <b>GetAtEndOfPayload</b> sets its output parameter to TRUE, Media Foundation will not invoke <b>BeginReadPayload</b> again.


## -parameters




### -param pfAtEndOfPayload [out]

Set to FALSE if a call to <a href="https://msdn.microsoft.com/01B799C2-63C6-4BDC-AAE2-CFC3C426A218">BeginReadPayload</a> can return one or more bytes of data to Media Foundation. Set to TRUE when there is no more data to return.


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

                The <i>pfAtEndOfPayload</i> parameter is an invalid pointer.

</td>
</tr>
</table>
 




## -remarks



Microsoft Media Foundation invokes <b>GetAtEndOfPayload</b> only after having successfully invoked <a href="https://msdn.microsoft.com/FC342FB9-930F-4EA7-9057-51AF10D13ED9">EndReceiveResponse</a>.




## -see-also




<a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a>
 

 

