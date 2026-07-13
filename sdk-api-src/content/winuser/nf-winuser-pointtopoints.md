---
UID: NF:winuser.POINTTOPOINTS
title: POINTTOPOINTS macro (winuser.h)
description: The POINTTOPOINTS macro converts a POINT structure to a POINTS structure.
helpviewer_keywords: ["POINTTOPOINTS","POINTTOPOINTS macro [Windows GDI]","_win32_POINTTOPOINTS","gdi.pointtopoints","winuser/POINTTOPOINTS"]
old-location: gdi\pointtopoints.htm
tech.root: gdi
ms.assetid: 9e9ec2c0-fce6-4205-8299-20ef7ff154e9
ms.date: 07/01/2025
ms.keywords: POINTTOPOINTS, POINTTOPOINTS macro [Windows GDI], _win32_POINTTOPOINTS, gdi.pointtopoints, winuser/POINTTOPOINTS
req.header: winuser.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - POINTTOPOINTS
 - winuser/POINTTOPOINTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - POINTTOPOINTS
---

# POINTTOPOINTS macro

## -syntax

```cpp
POINTS POINTTOPOINTS(
    POINT pt
);
```

## -returns

Type: **POINTS**

The return value is a <a href="/windows/win32/api/windef/ns-windef-points">POINTS</a> structure.


## -description

The <b>POINTTOPOINTS</b> macro converts a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure to a <a href="/windows/win32/api/windef/ns-windef-points">POINTS</a> structure.

## -parameters

### -param pt

The <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure to convert.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-makepoints">MAKEPOINTS</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/win32/api/windef/ns-windef-points">POINTS</a>



<a href="/windows/desktop/gdi/rectangle-macros">Rectangle Macros</a>



<a href="/windows/desktop/gdi/rectangles">Rectangles Overview</a>
