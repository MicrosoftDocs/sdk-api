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

# DdCreateSurfaceObject function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="https://msdn.microsoft.com/1b2886a8-279b-4bec-9fb8-b88a68ded25b">NtGdiDdCreateSurfaceObject</a> function and creates a kernel-mode surface object.


<b>GdiEntry4</b> is defined as an alias for this function.


## -parameters




### -param pSurfaceLocal

Pointer to the user-mode surface object. See the DDK documentation for details. A handle to the kernel-mode object is placed in <i>pSurfaceLocal</i>-&gt;<b>hDDSurface</b>.


### -param bPrimarySurface

Reserved.


## -returns



If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.




## -remarks



This function is used to create objects that represent system memory surfaces. Video memory surfaces are given a kernel-mode representation as an implicit part of the <a href="https://msdn.microsoft.com/1b2886a8-279b-4bec-9fb8-b88a68ded25b">NtGdiDdCreateSurfaceObject</a> call.
        

Applications are advised to use the 
DirectDraw and 
<a href="http://msdn.microsoft.com/en-us/library/bb205147(VS.85).aspx">Direct3D</a>
     
    APIs to create and manage graphics device objects. These constructs abstract the device creation process in a simplified and operating-system-independent way.
        




## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

