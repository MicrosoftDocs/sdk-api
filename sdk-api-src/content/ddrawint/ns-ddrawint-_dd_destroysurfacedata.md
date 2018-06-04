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

# _DD_DESTROYSURFACEDATA structure


## -description


The DD_DESTROYSURFACEDATA structure contains information necessary to destroy the specified surface--in the case of <a href="https://msdn.microsoft.com/f86c5c86-f0f2-4e2e-9235-a675d950bce1">DestroyD3DBuffer</a>, a command or vertex buffer.


## -struct-fields




### -field lpDD

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550586">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field lpDDSurface

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure representing the surface or buffer object to be destroyed. 


### -field ddRVal

Specifies the location in which the driver writes the return value of either the <a href="https://msdn.microsoft.com/90060863-02ef-49bf-820d-b3adffbc8f40">DdDestroySurface</a> or <a href="https://msdn.microsoft.com/f86c5c86-f0f2-4e2e-9235-a675d950bce1">DestroyD3DBuffer</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field DestroySurface

Used by the Microsoft DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/90060863-02ef-49bf-820d-b3adffbc8f40">DdDestroySurface</a>



<a href="https://msdn.microsoft.com/f86c5c86-f0f2-4e2e-9235-a675d950bce1">DestroyD3DBuffer</a>
 

 

