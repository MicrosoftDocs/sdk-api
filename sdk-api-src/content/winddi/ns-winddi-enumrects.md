---
UID: NS:winddi._ENUMRECTS
title: ENUMRECTS (winddi.h)
description: The ENUMRECTS structure is used by the CLIPOBJ_cEnumStart function to provide information about rectangles in a clip region for the CLIPOBJ_bEnum function.
helpviewer_keywords: ["ENUMRECTS","ENUMRECTS structure [Display Devices]","display.enumrects","grstrcts_8ea2422f-1b57-4a7a-be86-adca8b830a36.xml","winddi/ENUMRECTS"]
old-location: display\enumrects.htm
tech.root: display
ms.assetid: f7b8787f-f383-4cae-970e-8f4eb34b00da
ms.date: 12/05/2018
ms.keywords: ENUMRECTS, ENUMRECTS structure [Display Devices], display.enumrects, grstrcts_8ea2422f-1b57-4a7a-be86-adca8b830a36.xml, winddi/ENUMRECTS
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
req.typenames: ENUMRECTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENUMRECTS
 - winddi/_ENUMRECTS
 - ENUMRECTS
 - winddi/ENUMRECTS
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
 - ENUMRECTS
---

# ENUMRECTS structure


## -description

The ENUMRECTS structure is used by the <a href="/windows/desktop/api/winddi/nf-winddi-clipobj_cenumstart">CLIPOBJ_cEnumStart</a> function to provide information about rectangles in a clip region for the <a href="/windows/desktop/api/winddi/nf-winddi-clipobj_benum">CLIPOBJ_bEnum</a> function.

## -struct-fields

### -field c

Specifies the number of RECTL structures in the <b>arcl</b> array.

### -field arcl

Is an array of <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structures that specify the coordinates of rectangles in the clip region.