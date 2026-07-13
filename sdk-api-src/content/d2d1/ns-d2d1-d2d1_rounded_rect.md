---
UID: NS:d2d1.D2D1_ROUNDED_RECT
title: D2D1_ROUNDED_RECT (d2d1.h)
description: Contains the dimensions and corner radii of a rounded rectangle.
helpviewer_keywords: ["D2D1_ROUNDED_RECT","D2D1_ROUNDED_RECT structure [Direct2D]","d2d1/D2D1_ROUNDED_RECT","direct2d.D2D1_ROUNDED_RECT"]
old-location: direct2d\D2D1_ROUNDED_RECT.htm
tech.root: Direct2D
ms.assetid: 7069ca65-170e-42fc-8c1a-849a2f25c36f
ms.date: 12/05/2018
ms.keywords: D2D1_ROUNDED_RECT, D2D1_ROUNDED_RECT structure [Direct2D], d2d1/D2D1_ROUNDED_RECT, direct2d.D2D1_ROUNDED_RECT
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
req.typenames: D2D1_ROUNDED_RECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_ROUNDED_RECT
 - d2d1/D2D1_ROUNDED_RECT
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
 - D2D1_ROUNDED_RECT
---

## -description

Contains the dimensions and corner radii of a rounded rectangle.

## -struct-fields

### -field rect

Type: **[D2D1_RECT_F](/windows/win32/Direct2D/d2d1-rect-f)**

The coordinates of the rectangle.

### -field radiusX

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The x-radius for the quarter ellipse that is drawn to replace every corner of the rectangle.

### -field radiusY

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The y-radius for the quarter ellipse that is drawn to replace every corner of the rectangle.

## -remarks

Each corner of the rectangle specified by *rect* is replaced with a quarter ellipse, with a radius in each direction specified by *radiusX* and *radiusY*.

If *radiusX* is greater than or equal to half the width of the rectangle, and *radiusY* is greater than or equal to one-half the height, then the rounded rectangle is an ellipse with the same width and height of *rect*.

Even when both *radiusX* and *radiusY* are zero, the rounded rectangle is different from a rectangle. When stroked, the corners of the rounded rectangle are roundly joined, not mitered (square).
