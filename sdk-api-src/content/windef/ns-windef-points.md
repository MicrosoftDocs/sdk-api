---
UID: NS:windef.tagPOINTS
title: POINTS (windef.h)
description: The POINTS structure defines the x- and y-coordinates of a point.
helpviewer_keywords: ["*LPPOINTS","*PPOINTS","LPPOINTS","LPPOINTS structure pointer [Display Devices]","POINTS","POINTS structure [Display Devices]","PPOINTS","PPOINTS structure pointer [Display Devices]","display.points","grstrcts_ae45abcf-f0a0-4fbc-b9b8-f021d8f4f182.xml","windef/LPPOINTS","windef/POINTS","windef/PPOINTS"]
old-location: display\points.htm
tech.root: display
ms.assetid: 56d642a0-5281-44aa-af1e-61e1e83186af
ms.date: 12/05/2018
ms.keywords: '*LPPOINTS, *PPOINTS, LPPOINTS, LPPOINTS structure pointer [Display Devices], POINTS, POINTS structure [Display Devices], PPOINTS, PPOINTS structure pointer [Display Devices], display.points, grstrcts_ae45abcf-f0a0-4fbc-b9b8-f021d8f4f182.xml, windef/LPPOINTS, windef/POINTS, windef/PPOINTS'
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
req.typenames: POINTS, *PPOINTS, *LPPOINTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPOINTS
 - windef/tagPOINTS
 - PPOINTS
 - windef/PPOINTS
 - POINTS
 - windef/POINTS
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
 - POINTS
---

# POINTS structure


## -description

The POINTS structure defines the x- and y-coordinates of a point.

## -struct-fields

### -field y

Specifies the <i>y</i>-coordinate of the point.

### -field x

Specifies the <i>x</i>-coordinate of the point.

## -remarks

The POINTS structure is similar to the <a href="/windows/desktop/api/windef/ns-windef-point">POINT</a> and <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structures. The difference is that the members of the POINTS structure are of type SHORT, while those of the other two structures are of type LONG.

## -see-also

<a href="/windows/desktop/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a>