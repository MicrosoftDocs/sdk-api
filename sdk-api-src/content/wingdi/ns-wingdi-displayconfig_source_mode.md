---
UID: NS:wingdi.DISPLAYCONFIG_SOURCE_MODE
title: DISPLAYCONFIG_SOURCE_MODE
author: windows-sdk-content
description: The DISPLAYCONFIG_SOURCE_MODE structure represents a point or an offset in a two-dimensional space.
old-location: display\displayconfig_source_mode.htm
tech.root: display
ms.assetid: 413d63e5-da9d-4906-80a9-049da6e85275
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCD_Structures_c8b6e9f2-0855-478f-a091-78b57b19d596.xml, DISPLAYCONFIG_SOURCE_MODE, DISPLAYCONFIG_SOURCE_MODE structure [Display Devices], display.displayconfig_source_mode, wingdi/DISPLAYCONFIG_SOURCE_MODE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Client.
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
 - wingdi.h
api_name:
 - DISPLAYCONFIG_SOURCE_MODE
product: Windows
targetos: Windows
req.typenames: DISPLAYCONFIG_SOURCE_MODE
req.redist: 
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

A value from the <a href="https://msdn.microsoft.com/dca8433d-89a9-492c-bebb-6a28f485896c">DISPLAYCONFIG_PIXELFORMAT</a> enumeration that specifies the pixel format of the source mode.


### -field position

A <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure that specifies the position in the desktop coordinate space of the  upper-left corner of this source surface. The source surface that is located at (0, 0) is always the primary source surface.


## -remarks



The arrangement of source surfaces on the desktop is controlled by the <b>position</b> member, which specifies the position in desktop coordinates of the upper-left corner of the source surface. The source surface that is positioned at (0, 0) is considered the primary. GDI has strict rules about how the source surfaces can be arranged in the desktop space. For example, there cannot be any gaps between source surfaces, and there can be no overlaps.

The <a href="https://msdn.microsoft.com/9f649fa0-ffb2-44c6-9a66-049f888e3b04">SetDisplayConfig</a> function attempts to rearrange source surfaces in order to enforce these layout rules. The caller must make every effort to lay out the source surfaces correctly because  GDI  rearranges the sources in an undefined manner to enforce the layout rules. The resultant layout may not be what the caller wanted to achieve. 




## -see-also




<a href="https://msdn.microsoft.com/dca8433d-89a9-492c-bebb-6a28f485896c">DISPLAYCONFIG_PIXELFORMAT</a>



<a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a>



<a href="https://msdn.microsoft.com/9f649fa0-ffb2-44c6-9a66-049f888e3b04">SetDisplayConfig</a>
 

 

