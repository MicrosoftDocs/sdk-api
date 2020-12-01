---
UID: NF:wingdi.CreateEllipticRgn
title: CreateEllipticRgn function (wingdi.h)
description: The CreateEllipticRgn function creates an elliptical region.
helpviewer_keywords: ["CreateEllipticRgn","CreateEllipticRgn function [Windows GDI]","_win32_CreateEllipticRgn","gdi.createellipticrgn","wingdi/CreateEllipticRgn"]
old-location: gdi\createellipticrgn.htm
tech.root: gdi
ms.assetid: b4e9b210-8e22-42db-bb6e-65f1fb870eff
ms.date: 12/05/2018
ms.keywords: CreateEllipticRgn, CreateEllipticRgn function [Windows GDI], _win32_CreateEllipticRgn, gdi.createellipticrgn, wingdi/CreateEllipticRgn
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateEllipticRgn
 - wingdi/CreateEllipticRgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateEllipticRgn
---

# CreateEllipticRgn function


## -description

The <b>CreateEllipticRgn</b> function creates an elliptical region.

## -parameters

### -param x1 [in]

Specifies the x-coordinate in logical units, of the upper-left corner of the bounding rectangle of the ellipse.

### -param y1 [in]

Specifies the y-coordinate in logical units, of the upper-left corner of the bounding rectangle of the ellipse.

### -param x2 [in]

Specifies the x-coordinate in logical units, of the lower-right corner of the bounding rectangle of the ellipse.

### -param y2 [in]

Specifies the y-coordinate in logical units, of the lower-right corner of the bounding rectangle of the ellipse.

## -returns

If the function succeeds, the return value is the handle to the region.

If the function fails, the return value is <b>NULL</b>.

## -remarks

When you no longer need the HRGN object, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

A bounding rectangle defines the size, shape, and orientation of the region: The long sides of the rectangle define the length of the ellipse's major axis; the short sides define the length of the ellipse's minor axis; and the center of the rectangle defines the intersection of the major and minor axes.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createellipticrgnindirect">CreateEllipticRegnIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>