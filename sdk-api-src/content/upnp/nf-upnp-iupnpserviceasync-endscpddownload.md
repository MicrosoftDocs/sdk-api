---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUPnPServiceAsync::EndSCPDDownload


## -description


The <b>EndSCPDDownload</b> method retrieves the results of  a previous asynchronous download of an Service Control Protocol Description (SCPD) document. 


## -parameters




### -param ullRequestID

Pointer to a 64-bit <b>ULONG</b> value that corresponds to the <a href="https://msdn.microsoft.com/CA573855-6D86-4C6C-B557-F8E8776BDBD3">BeginSCPDDownload</a> operation requested prior to this call.


### -param pbstrSCPDDoc [out]

A  buffer containing the SCPD document.


## -returns



Returns <b>S_OK</b> on success. Otherwise, the method returns a COM error code defined in <b>WinError.h</b> or one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failed to finalize the SCPD download and retrieve the document string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ullRequestID</i> does not match the pending async call.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/B77025D6-26C7-46C9-84FE-69685C61735D">IUPnPServiceAsync</a>



<a href="https://msdn.microsoft.com/CA573855-6D86-4C6C-B557-F8E8776BDBD3">IUPnPServiceAsync::BeginSCPDDownload</a>
 

 

