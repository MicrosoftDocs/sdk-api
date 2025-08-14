---
UID: NF:winuser.POINTSTOPOINT
title: POINTSTOPOINT macro (winuser.h)
description: The POINTSTOPOINT macro copies the contents of a POINTS structure into a POINT structure.
helpviewer_keywords: ["POINTSTOPOINT","POINTSTOPOINT macro [Windows GDI]","_win32_POINTSTOPOINT","gdi.pointstopoint","winuser/POINTSTOPOINT"]
old-location: gdi\pointstopoint.htm
tech.root: gdi
ms.assetid: 921da8a5-cd8a-4851-b470-9b7bd10afaad
ms.date: 07/01/2025
ms.keywords: POINTSTOPOINT, POINTSTOPOINT macro [Windows GDI], _win32_POINTSTOPOINT, gdi.pointstopoint, winuser/POINTSTOPOINT
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
 - POINTSTOPOINT
 - winuser/POINTSTOPOINT
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
 - POINTSTOPOINT
---

# POINTSTOPOINT macro

## -syntax

```cpp
void POINTSTOPOINT(
    POINT pt,
    POINTS pts
);
```


## -description

The <b>POINTSTOPOINT</b> macro copies the contents of a <a href="/windows/win32/api/windef/ns-windef-points">POINTS</a> structure into a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure.

## -parameters

### -param pt

The <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure to receive the contents of the <a href="/windows/win32/api/windef/ns-windef-points">POINTS</a> structure.

### -param pts

The <a href="/windows/win32/api/windef/ns-windef-points">POINTS</a> structure to copy.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-makepoints">MAKEPOINTS</a>



<a href="/windows/desktop/api/winuser/nf-winuser-pointtopoints">POINTTOPOINTS</a>



<a href="/windows/desktop/gdi/rectangle-macros">Rectangle Macros</a>



<a href="/windows/desktop/gdi/rectangles">Rectangles Overview</a>
