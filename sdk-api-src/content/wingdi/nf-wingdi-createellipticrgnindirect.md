---
UID: NF:wingdi.CreateEllipticRgnIndirect
title: CreateEllipticRgnIndirect function (wingdi.h)
description: The CreateEllipticRgnIndirect function creates an elliptical region.
helpviewer_keywords: ["CreateEllipticRgnIndirect","CreateEllipticRgnIndirect function [Windows GDI]","_win32_CreateEllipticRgnIndirect","gdi.createellipticrgnindirect","wingdi/CreateEllipticRgnIndirect"]
old-location: gdi\createellipticrgnindirect.htm
tech.root: gdi
ms.assetid: bd30516e-1e05-4b7d-a6bf-7512cf3ef30f
ms.date: 12/05/2018
ms.keywords: CreateEllipticRgnIndirect, CreateEllipticRgnIndirect function [Windows GDI], _win32_CreateEllipticRgnIndirect, gdi.createellipticrgnindirect, wingdi/CreateEllipticRgnIndirect
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
 - CreateEllipticRgnIndirect
 - wingdi/CreateEllipticRgnIndirect
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
 - CreateEllipticRgnIndirect
---

# CreateEllipticRgnIndirect function


## -description

The <b>CreateEllipticRgnIndirect</b> function creates an elliptical region.

## -parameters

### -param lprect [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the coordinates of the upper-left and lower-right corners of the bounding rectangle of the ellipse in logical units.

## -returns

If the function succeeds, the return value is the handle to the region.

If the function fails, the return value is <b>NULL</b>.

## -remarks

When you no longer need the <b>HRGN</b> object, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

A bounding rectangle defines the size, shape, and orientation of the region: The long sides of the rectangle define the length of the ellipse's major axis; the short sides define the length of the ellipse's minor axis; and the center of the rectangle defines the intersection of the major and minor axes.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createellipticrgn">CreateEllipticRegn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>