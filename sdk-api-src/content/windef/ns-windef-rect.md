---
UID: NS:windef.tagRECT
title: RECT (windef.h)
description: The RECT structure defines a rectangle by the coordinates of its upper-left and lower-right corners.
helpviewer_keywords: ["*LPRECT","*NPRECT","*PRECT","FAR *LPRECT","FAR *LPRECT structure [Display Devices]","NEAR *NPRECT","NEAR *NPRECT structure [Display Devices]","PRECT","PRECT structure pointer [Display Devices]","RECT","RECT structure [Display Devices]","display.rect","grstrcts_9bf844e0-1ec8-4bc0-a0ce-0790a4cfc93e.xml","windef/FAR *LPRECT","windef/NEAR *NPRECT","windef/PRECT","windef/RECT"]
old-location: display\rect.htm
tech.root: display
ms.assetid: a44f33f4-49b2-4a36-a7bd-fc4a9d3a3943
ms.date: 12/05/2018
ms.keywords: '*LPRECT, *NPRECT, *PRECT, FAR *LPRECT, FAR *LPRECT structure [Display Devices], NEAR *NPRECT, NEAR *NPRECT structure [Display Devices], PRECT, PRECT structure pointer [Display Devices], RECT, RECT structure [Display Devices], display.rect, grstrcts_9bf844e0-1ec8-4bc0-a0ce-0790a4cfc93e.xml, windef/FAR *LPRECT, windef/NEAR *NPRECT, windef/PRECT, windef/RECT'
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
req.typenames: RECT, *PRECT, *NPRECT, *LPRECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRECT
 - windef/tagRECT
 - PRECT
 - windef/PRECT
 - RECT
 - windef/RECT
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
 - RECT
---

# RECT structure


## -description

The RECT structure defines a rectangle by the coordinates of its upper-left and lower-right corners.

## -struct-fields

### -field left

Specifies the <i>x</i>-coordinate of the upper-left corner of the rectangle.

### -field top

Specifies the <i>y</i>-coordinate of the upper-left corner of the rectangle.

### -field right

Specifies the <i>x</i>-coordinate of the lower-right corner of the rectangle.

### -field bottom

Specifies the <i>y</i>-coordinate of the lower-right corner of the rectangle.

## -remarks

The RECT structure is identical to the <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure.

## -see-also

<a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a>