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

# TcDeleteFilter function


## -description


The 
<b>TcDeleteFilter</b> function deletes a filter previously added with the 
<a href="https://msdn.microsoft.com/c6d7c346-c353-4224-a8b5-56910e447902">TcAddFilter</a> function.


## -parameters




### -param FilterHandle [in]

Handle to the filter to be deleted, as received in a previous call to the 
<a href="https://msdn.microsoft.com/c6d7c346-c353-4224-a8b5-56910e447902">TcAddFilter</a> function.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function executed without errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The filter handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Use of the 
<b>TcDeleteFilter</b> function requires administrative privilege.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c6d7c346-c353-4224-a8b5-56910e447902">TcAddFilter</a>
 

 

