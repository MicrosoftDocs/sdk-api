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

# DdAttachSurface function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

The <b>DdAttachSurface</b> function attaches two kernel-mode surface representations.



<b>GdiEntry11</b> is defined as an alias for this function.


## -parameters




### -param pSurfaceFrom [in]

Pointer to a kernel-mode surface object that will be the start point of the new attachment.


### -param pSurfaceTo [in]

Pointer to a kernel-mode surface object that will be the end point of the new attachment.


## -returns



<b>DdAttachSurface</b> returns one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The function call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The function call failed.

</td>
</tr>
</table>
 




## -remarks



See the DirectDraw 
    software development kit (SDK) and Driver Development Kit (DDK) for a full description of surface attachments.

<div class="alert"><b>Note</b>  As with other surface attachments, the resulting attachment is one-way.  After this function is called, <i>pSurfaceTo</i> will not be attached to <i>pSurfaceFrom</i>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

