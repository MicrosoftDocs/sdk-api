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

# DdUnattachSurface function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

The <b>DdUnattachSurface</b> function removes an attachment, created with <a href="https://msdn.microsoft.com/549c34ad-3e41-4602-951b-15f1f62ec777">DdAttachSurface</a>, between two kernel-mode surface objects.

<b>GdiEntry12</b> is defined as an alias for this function.


## -parameters




### -param pSurface [in]

Pointer to the kernel-mode surface object that was passed as the <i>pSurfaceFrom</i> parameter to <a href="https://msdn.microsoft.com/549c34ad-3e41-4602-951b-15f1f62ec777">DdAttachSurface</a>.


### -param pSurfaceAttached [in]

Pointer to the kernel-mode surface object that was passed as the <i>pSurfaceTo</i> parameter to <a href="https://msdn.microsoft.com/549c34ad-3e41-4602-951b-15f1f62ec777">DdAttachSurface</a>



## -returns



This function does not return a value.




## -remarks



It is recommended that applications use the DirectDraw 
    API which handles surface attachments in a higher-level manner.

It is not necessary to call this function since the kernel will automatically destroy all attachments when <a href="https://msdn.microsoft.com/65419fce-9e82-4621-9906-832144888a3b">DdDestroySurface</a> is called.




## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

