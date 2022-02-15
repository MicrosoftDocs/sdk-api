---
UID: NE:d2d1.D2D1_CAP_STYLE
title: D2D1_CAP_STYLE (d2d1.h)
description: Describes the shape at the end of a line or segment.
helpviewer_keywords: ["D2D1_CAP_STYLE","D2D1_CAP_STYLE enumeration [Direct2D]","D2D1_CAP_STYLE_FLAT","D2D1_CAP_STYLE_ROUND","D2D1_CAP_STYLE_SQUARE","D2D1_CAP_STYLE_TRIANGLE","d2d1/D2D1_CAP_STYLE","d2d1/D2D1_CAP_STYLE_FLAT","d2d1/D2D1_CAP_STYLE_ROUND","d2d1/D2D1_CAP_STYLE_SQUARE","d2d1/D2D1_CAP_STYLE_TRIANGLE","direct2d.D2D1_CAP_STYLE"]
old-location: direct2d\D2D1_CAP_STYLE.htm
tech.root: Direct2D
ms.assetid: acf4365e-b9df-459e-a746-016339cd09ac
ms.date: 12/05/2018
ms.keywords: D2D1_CAP_STYLE, D2D1_CAP_STYLE enumeration [Direct2D], D2D1_CAP_STYLE_FLAT, D2D1_CAP_STYLE_ROUND, D2D1_CAP_STYLE_SQUARE, D2D1_CAP_STYLE_TRIANGLE, d2d1/D2D1_CAP_STYLE, d2d1/D2D1_CAP_STYLE_FLAT, d2d1/D2D1_CAP_STYLE_ROUND, d2d1/D2D1_CAP_STYLE_SQUARE, d2d1/D2D1_CAP_STYLE_TRIANGLE, direct2d.D2D1_CAP_STYLE
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: D2D1_CAP_STYLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_CAP_STYLE
 - d2d1/D2D1_CAP_STYLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_CAP_STYLE
---

# D2D1_CAP_STYLE enumeration


## -description

Describes the shape at the end of a line or segment.

## -enum-fields

### -field D2D1_CAP_STYLE_FLAT:0

A cap that does not extend past the last point of the line. Comparable to cap used for objects other than lines.

### -field D2D1_CAP_STYLE_SQUARE:1

Half of a square that has a length equal to the line thickness.

### -field D2D1_CAP_STYLE_ROUND:2

A semicircle that has a diameter equal to the line thickness.

### -field D2D1_CAP_STYLE_TRIANGLE:3

An isosceles right triangle whose hypotenuse is equal in length to the thickness of the line.

### -field D2D1_CAP_STYLE_FORCE_DWORD:0xffffffff

## -remarks

The following illustration shows the available cap styles for lines or segments. The red portion of the line shows the extra area added by the line cap setting.



<img alt="Illustration of four cap styles" src="./images/linecaps.png"/>

