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

# DISPLAYCONFIG_PIXELFORMAT enumeration


## -description


The DISPLAYCONFIG_PIXELFORMAT enumeration specifies pixel format in various bits per pixel (BPP) values.


## -enum-fields




### -field DISPLAYCONFIG_PIXELFORMAT_8BPP

Indicates 8 BPP format. 


### -field DISPLAYCONFIG_PIXELFORMAT_16BPP

Indicates 16 BPP format. 


### -field DISPLAYCONFIG_PIXELFORMAT_24BPP

Indicates 24 BPP format. 


### -field DISPLAYCONFIG_PIXELFORMAT_32BPP

Indicates 32 BPP format. 


### -field DISPLAYCONFIG_PIXELFORMAT_NONGDI

Indicates that the current display is not an 8, 16, 24, or 32 BPP GDI desktop mode. For example, a call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569215">QueryDisplayConfig</a> function returns DISPLAYCONFIG_PIXELFORMAT_NONGDI if a DirectX application previously set the desktop to A2R10G10B10 format. A call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569533">SetDisplayConfig</a> function fails if any pixel formats for active paths are set to DISPLAYCONFIG_PIXELFORMAT_NONGDI. 


### -field DISPLAYCONFIG_PIXELFORMAT_FORCE_UINT32

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff569215">QueryDisplayConfig</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569533">SetDisplayConfig</a>
 

 

