---
UID: NS:winddi._GLYPHPOS
title: GLYPHPOS (winddi.h)
description: The GLYPHPOS structure is used by GDI to provide a graphics driver with a glyph's description and position.
helpviewer_keywords: ["*PGLYPHPOS","GLYPHPOS","GLYPHPOS structure [Display Devices]","PGLYPHPOS","PGLYPHPOS structure pointer [Display Devices]","display.glyphpos","grstrcts_52c5687f-a40b-43c6-8513-accd4c72def5.xml","winddi/GLYPHPOS","winddi/PGLYPHPOS"]
old-location: display\glyphpos.htm
tech.root: display
ms.assetid: 1eb80e7a-93f5-474c-bed9-5b19f6657788
ms.date: 12/05/2018
ms.keywords: '*PGLYPHPOS, GLYPHPOS, GLYPHPOS structure [Display Devices], PGLYPHPOS, PGLYPHPOS structure pointer [Display Devices], display.glyphpos, grstrcts_52c5687f-a40b-43c6-8513-accd4c72def5.xml, winddi/GLYPHPOS, winddi/PGLYPHPOS'
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
targetos: Windows
req.typenames: GLYPHPOS, *PGLYPHPOS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GLYPHPOS
 - winddi/_GLYPHPOS
 - PGLYPHPOS
 - winddi/PGLYPHPOS
 - GLYPHPOS
 - winddi/GLYPHPOS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - GLYPHPOS
---

# GLYPHPOS structure


## -description

The GLYPHPOS structure is used by GDI to provide a graphics driver with a glyph's description and position.

## -struct-fields

### -field hg

Handle to the glyph.

### -field pgdf

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-glyphdef">GLYPHDEF</a> union.

### -field ptl

Specifies a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that contains the coordinates of the point in device space where the character origin of the glyph should be placed.

## -remarks

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>



<a href="/windows/desktop/api/winddi/ns-winddi-glyphdef">GLYPHDEF</a>



<a href="/windows/desktop/api/winddi/ns-winddi-strobj">STROBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-strobj_benum">STROBJ_bEnum</a>



<a href="/windows/desktop/api/winddi/nf-winddi-strobj_venumstart">STROBJ_vEnumStart</a>