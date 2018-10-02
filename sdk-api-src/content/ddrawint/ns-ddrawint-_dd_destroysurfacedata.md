---
UID: NS:ddrawint._DD_DESTROYSURFACEDATA
title: "_DD_DESTROYSURFACEDATA"
author: windows-sdk-content
description: The DD_DESTROYSURFACEDATA structure contains information necessary to destroy the specified surface--in the case of DestroyD3DBuffer, a command or vertex buffer.
old-location: display\dd_destroysurfacedata.htm
tech.root: Display
ms.assetid: 77d9544d-72df-4e7d-ba57-644aeee34a88
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDD_DESTROYSURFACEDATA, DD_DESTROYSURFACEDATA, DD_DESTROYSURFACEDATA structure [Display Devices], _DD_DESTROYSURFACEDATA, ddrawint/DD_DESTROYSURFACEDATA, ddstrcts_19c2445b-0f9f-445d-a486-8ca100beeca7.xml, display.dd_destroysurfacedata"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_DESTROYSURFACEDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_DESTROYSURFACEDATA, DD_DESTROYSURFACEDATA"
req.redist: 
---

# _DD_DESTROYSURFACEDATA structure


## -description


The DD_DESTROYSURFACEDATA structure contains information necessary to destroy the specified surface--in the case of <a href="https://msdn.microsoft.com/f86c5c86-f0f2-4e2e-9235-a675d950bce1">DestroyD3DBuffer</a>, a command or vertex buffer.


## -struct-fields




### -field lpDD

Points to the <a href="https://msdn.microsoft.com/a59f064b-48cf-4491-82cd-84f59467af87">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field lpDDSurface

Points to the <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structure representing the surface or buffer object to be destroyed. 


### -field ddRVal

Specifies the location in which the driver writes the return value of either the <a href="https://msdn.microsoft.com/90060863-02ef-49bf-820d-b3adffbc8f40">DdDestroySurface</a> or <a href="https://msdn.microsoft.com/f86c5c86-f0f2-4e2e-9235-a675d950bce1">DestroyD3DBuffer</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field DestroySurface

Used by the Microsoft DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/90060863-02ef-49bf-820d-b3adffbc8f40">DdDestroySurface</a>



<a href="https://msdn.microsoft.com/f86c5c86-f0f2-4e2e-9235-a675d950bce1">DestroyD3DBuffer</a>
 

 

