---
UID: NF:mfidl.IMFHttpDownloadRequest.GetRangeEndOffset
title: IMFHttpDownloadRequest::GetRangeEndOffset
author: windows-sdk-content
description: Invoked by Microsoft Media Foundation to retrieve the offset of the last byte in the current response, counted from the start of the resource. This is useful when a request uses the HTTP “Range” header to download only a portion of a resource.
old-location: mf\imfhttpdownloadrequest_getrangeendoffset.htm
old-project: medfound
ms.assetid: 015CBC40-BE9E-4C9F-AC1B-30FFDD2B11CC
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetRangeEndOffset, GetRangeEndOffset method [Media Foundation], GetRangeEndOffset method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],GetRangeEndOffset method, IMFHttpDownloadRequest.GetRangeEndOffset, IMFHttpDownloadRequest::GetRangeEndOffset, mf.imfhttpdownloadrequest_getrangeendoffset, mfidl/IMFHttpDownloadRequest::GetRangeEndOffset
ms.prod: windows
ms.technology: windows-sdk
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
-	IMFHttpDownloadRequest.GetRangeEndOffset
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFHttpDownloadRequest::GetRangeEndOffset


## -description


Invoked by Microsoft Media Foundation to retrieve the offset of the last byte in the current response, counted from the start of the resource. This is useful when a request uses the HTTP “Range” header to download only a portion of a resource.


## -parameters




### -param pqwRangeEnd






#### - qwpRangeEnd [out]

The offset of the last byte in the current response, counted from the start of the resource, if known. For example, if the request specified the HTTP header, “Range: bytes=1000-“ and the size of the message body in the response is 200 bytes, then <i>pwqRangeEnd</i> becomes 1199. If the value is not known, for example, because the server did not specify the size of its response, <i>pwqRangeEnd</i> is set to MAX_ULONG (0xFFFFFFFFFFFFFFFF).


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

                The <i>qwpRangeEnd</i> parameter is an invalid pointer.

</td>
</tr>
</table>
 




## -remarks



Microsoft Media Foundation invokes <b>GetRangeEndOffset</b> only after having successfully invoked <a href="https://msdn.microsoft.com/FC342FB9-930F-4EA7-9057-51AF10D13ED9">EndReceiveResponse</a>.




## -see-also




<a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a>
 

 

