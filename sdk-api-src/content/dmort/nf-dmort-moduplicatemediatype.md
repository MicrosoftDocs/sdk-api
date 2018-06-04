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

# MoDuplicateMediaType function


## -description


The <b>MoDuplicateMediaType</b> function duplicates a media type structure.


## -parameters




### -param ppmtDest

Address of a pointer to a <a href="https://msdn.microsoft.com/c545ddf7-9797-45ab-a42a-d8550b598e98">DMO_MEDIA_TYPE</a> structure that receives the duplicated structure.


### -param pmtSrc

Pointer to the media type structure to duplicate.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



This method is equivalent to calling <a href="https://msdn.microsoft.com/f67b04b5-163e-4793-8df0-10a4b2be5025">MoCreateMediaType</a> and <a href="https://msdn.microsoft.com/7b6325bf-a996-467e-896d-a6dc41f63fd4">MoCopyMediaType</a>. The caller must delete the returned media type structure by calling the <a href="https://msdn.microsoft.com/adbfe1e1-e956-48de-9ed1-9f8f4c66ff1c">MoDeleteMediaType</a> function.



