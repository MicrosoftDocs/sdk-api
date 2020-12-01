---
UID: NS:windef.tagSIZE
title: SIZE (windef.h)
description: The SIZE structure defines the width and height of a rectangle.
helpviewer_keywords: ["*LPSIZE","*PSIZE","*PSIZEL","LPSIZE","LPSIZE structure pointer [Display Devices]","PSIZE","PSIZE structure pointer [Display Devices]","SIZE","SIZE structure [Display Devices]","SIZEL","display.size","grstrcts_2697a459-d1f4-4617-8370-d51a3c79f609.xml","windef/LPSIZE","windef/PSIZE","windef/SIZE"]
old-location: display\size.htm
tech.root: display
ms.assetid: 08d81096-069f-4554-9bb9-d4a37c0950ac
ms.date: 12/05/2018
ms.keywords: '*LPSIZE, *PSIZE, *PSIZEL, LPSIZE, LPSIZE structure pointer [Display Devices], PSIZE, PSIZE structure pointer [Display Devices], SIZE, SIZE structure [Display Devices], SIZEL, display.size, grstrcts_2697a459-d1f4-4617-8370-d51a3c79f609.xml, windef/LPSIZE, windef/PSIZE, windef/SIZE'
req.header: windef.h
req.include-header: Windows.h
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
req.typenames: SIZE, *PSIZE, *LPSIZE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSIZE
 - windef/tagSIZE
 - PSIZE
 - windef/PSIZE
 - SIZE
 - windef/SIZE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windef.h
api_name:
 - SIZE
---

# SIZE structure


## -description

The SIZE structure defines the width and height of a rectangle.

## -struct-fields

### -field cx

Specifies the rectangle's width. The units depend on which function uses this structure.

### -field cy

Specifies the rectangle's height. The units depend on which function uses this structure.

## -remarks

The rectangle dimensions stored in this structure can correspond to viewport extents, window extents, text extents, bitmap dimensions, or the aspect-ratio filter for some extended functions.

## -see-also

<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a>