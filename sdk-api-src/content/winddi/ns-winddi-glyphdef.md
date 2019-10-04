---
UID: NS:winddi._GLYPHDEF
title: GLYPHDEF (winddi.h)
author: windows-sdk-content
description: The GLYPHDEF union identifies individual glyphs and provides either a pointer to a GLYPHBITS structure or a pointer to a PATHOBJ structure.
old-location: display\glyphdef.htm
tech.root: display
ms.assetid: d1a7a02c-acaf-46b5-9ffe-fddbb01408a5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GLYPHDEF, GLYPHDEF union [Display Devices], display.glyphdef, grstrcts_d3283f02-3635-482d-a65a-b92f0a91aa54.xml, winddi/GLYPHDEF
ms.topic: struct
f1_keywords:
- winddi/GLYPHDEF
dev_langs:
 - c++
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
- GLYPHDEF
targetos: Windows
req.typenames: GLYPHDEF
req.redist: 
ms.custom: 19H1
---

# GLYPHDEF structure


## -description


The GLYPHDEF union identifies individual glyphs and provides either a pointer to a GLYPHBITS structure or a pointer to a PATHOBJ structure.


## -struct-fields




### -field pgb

If <b>pgb</b> is defined, this member is a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-glyphbits">GLYPHBITS</a> structure. The driver can use the bitmap bits stored in this structure to form the associated glyph on its surface.


### -field ppo

If <b>ppo</b> is defined, this member is a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure the driver can examine to extract the path describing the associated glyph.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-glyphbits">GLYPHBITS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>
 

 

