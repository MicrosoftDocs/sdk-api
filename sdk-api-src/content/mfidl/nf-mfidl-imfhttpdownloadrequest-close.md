---
UID: NF:mfidl.IMFHttpDownloadRequest.Close
title: IMFHttpDownloadRequest::Close
author: windows-sdk-content
description: Invoked by Microsoft Media Foundation to allow IMFHttpDownloadRequest to free any internal resources. It will also cancel the current request if it is still in progress.
old-location: mf\imfhttpdownloadrequest_close.htm
tech.root: medfound
ms.assetid: BA560323-EE64-4423-B63A-F2B6FDE608DC
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Close, Close method [Media Foundation], Close method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],Close method, IMFHttpDownloadRequest.Close, IMFHttpDownloadRequest::Close, mf.imfhttpdownloadrequest_close, mfidl/IMFHttpDownloadRequest::Close
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
 - IMFHttpDownloadRequest.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFHttpDownloadRequest.Close
: 
---

# IMFHttpDownloadRequest::Close


## -description


Invoked by Microsoft Media Foundation to allow <a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a> to free any internal resources. It will also cancel the current request if it is still in progress.


## -parameters






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
Successfully closed the request object.

</td>
</tr>
</table>
 




## -remarks



Microsoft Media Foundation will not invoke any other methods on the <a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a> interface after having invoked <b>Close</b>.




## -see-also




<a href="https://msdn.microsoft.com/A8A37C2F-A662-4FDA-95F6-43D96A8471A8">IMFHttpDownloadRequest</a>
 

 

