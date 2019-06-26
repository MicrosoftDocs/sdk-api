---
UID: NF:mfidl.IMFHttpDownloadSession.Close
title: IMFHttpDownloadSession::Close (mfidl.h)
author: windows-sdk-content
description: Invoked by Microsoft Media Foundation to specify that no more HTTP requests will be created, and allows IMFHttpDownloadSession to free any internal resources.
old-location: mf\imfhttpdownloadsession_close.htm
tech.root: medfound
ms.assetid: 587D281D-0488-470B-9E20-AE6DE70F33DC
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Close, Close method [Media Foundation], Close method [Media Foundation],IMFHttpDownloadSession interface, IMFHttpDownloadSession interface [Media Foundation],Close method, IMFHttpDownloadSession.Close, IMFHttpDownloadSession::Close, mf.imfhttpdownloadsession_close, mfidl/IMFHttpDownloadSession::Close
ms.topic: method
f1_keywords: 
 - "mfidl/IMFHttpDownloadSession.Close"
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
 - IMFHttpDownloadSession.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFHttpDownloadSession::Close


## -description


Invoked by Microsoft Media Foundation to specify that no more HTTP requests will be created, and allows <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession">IMFHttpDownloadSession</a> to free any internal resources.


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
Successfully closed the session.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession">IMFHttpDownloadSession</a>
 

 

