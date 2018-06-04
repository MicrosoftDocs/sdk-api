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

# DdGetDxHandle function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Returns the kernel-mode Microsoft DirectX 
   API handle to use in subsequent calls to the kernel-mode entry points that control the DirectX 
   API mechanism.

<b>GdiEntry14</b> is defined as an alias for this function.


## -parameters




### -param pDDraw [in]

Pointer to the DirectDraw object owning the surface. This parameter is optional and may be set to <b>NULL</b>.


### -param pSurface [in]

Pointer to the surface for which to return a kernel-mode DirectX API handle. This parameter is optional and may be set to <b>NULL</b>.


### -param bRelease [in]

Set to <b>TRUE</b> if the DirectX API kernel mode interface should be released. Otherwise, <b>FALSE</b>.


## -returns



A DirectX API handle used in subsequent DirectX API-oriented kernel entry points.




## -remarks



If both <i>pDDraw</i> and <i>pSurface</i> are specified, <i>pSurface</i> is ignored.




## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

