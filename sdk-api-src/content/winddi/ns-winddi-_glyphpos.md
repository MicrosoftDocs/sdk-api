---
UID: NS:winddi._GLYPHPOS
title: "_GLYPHPOS"
author: windows-sdk-content
description: The GLYPHPOS structure is used by GDI to provide a graphics driver with a glyph's description and position.
old-location: display\glyphpos.htm
tech.root: display
ms.assetid: 1eb80e7a-93f5-474c-bed9-5b19f6657788
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PGLYPHPOS, GLYPHPOS, GLYPHPOS structure [Display Devices], PGLYPHPOS, PGLYPHPOS structure pointer [Display Devices], _GLYPHPOS, display.glyphpos, grstrcts_52c5687f-a40b-43c6-8513-accd4c72def5.xml, winddi/GLYPHPOS, winddi/PGLYPHPOS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winddi.h
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
 - winddi.h
api_name:
 - GLYPHPOS
product: Windows
targetos: Windows
req.typenames: GLYPHPOS, *PGLYPHPOS
req.redist: 
---

# _GLYPHPOS structure


## -description


The GLYPHPOS structure is used by GDI to provide a graphics driver with a glyph's description and position.


## -struct-fields




### -field hg

Handle to the glyph.


### -field pgdf

Pointer to a <a href="https://msdn.microsoft.com/d1a7a02c-acaf-46b5-9ffe-fddbb01408a5">GLYPHDEF</a> union.


### -field ptl

Specifies a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure that contains the coordinates of the point in device space where the character origin of the glyph should be placed.


## -remarks








## -see-also




<a href="https://msdn.microsoft.com/f2f61687-d833-4d09-8cd5-99e81436c1c1">DrvTextOut</a>



<a href="https://msdn.microsoft.com/d1a7a02c-acaf-46b5-9ffe-fddbb01408a5">GLYPHDEF</a>



<a href="https://msdn.microsoft.com/efe53cb8-39b9-4931-bac2-9c61efd9d457">STROBJ</a>



<a href="https://msdn.microsoft.com/82cb12ff-2baa-4291-849c-dab9d01fa39b">STROBJ_bEnum</a>



<a href="https://msdn.microsoft.com/568af273-2b9d-4782-849f-6cb9c49952e0">STROBJ_vEnumStart</a>
 

 

