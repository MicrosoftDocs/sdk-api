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

# DISPLAYCONFIG_SOURCE_MODE structure


## -description


The <b>DISPLAYCONFIG_SOURCE_MODE</b> structure represents a point or an offset in a two-dimensional space.


## -struct-fields




### -field width

The width in pixels of the source mode.


### -field height

The height in pixels of the source mode.


### -field pixelFormat

A value from the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553963">DISPLAYCONFIG_PIXELFORMAT</a> enumeration that specifies the pixel format of the source mode.


### -field position

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that specifies the position in the desktop coordinate space of the  upper-left corner of this source surface. The source surface that is located at (0, 0) is always the primary source surface.


## -remarks



The arrangement of source surfaces on the desktop is controlled by the <b>position</b> member, which specifies the position in desktop coordinates of the upper-left corner of the source surface. The source surface that is positioned at (0, 0) is considered the primary. GDI has strict rules about how the source surfaces can be arranged in the desktop space. For example, there cannot be any gaps between source surfaces, and there can be no overlaps.

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff569533">SetDisplayConfig</a> function attempts to rearrange source surfaces in order to enforce these layout rules. The caller must make every effort to lay out the source surfaces correctly because  GDI  rearranges the sources in an undefined manner to enforce the layout rules. The resultant layout may not be what the caller wanted to achieve. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff553963">DISPLAYCONFIG_PIXELFORMAT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569533">SetDisplayConfig</a>
 

 

