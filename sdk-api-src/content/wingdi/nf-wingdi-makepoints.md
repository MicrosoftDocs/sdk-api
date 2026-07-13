---
UID: NF:wingdi.MAKEPOINTS
title: MAKEPOINTS macro (wingdi.h)
description: The MAKEPOINTS macro converts a value that contains the x- and y-coordinates of a point into a POINTS structure.
helpviewer_keywords: ["MAKEPOINTS","MAKEPOINTS macro [Windows GDI]","_win32_MAKEPOINTS","gdi.makepoints","wingdi/MAKEPOINTS"]
old-location: gdi\makepoints.htm
tech.root: gdi
ms.assetid: 1f84cfd0-2836-4c20-9408-17e0d57742be
ms.date: 07/01/2025
ms.keywords: MAKEPOINTS, MAKEPOINTS macro [Windows GDI], _win32_MAKEPOINTS, gdi.makepoints, wingdi/MAKEPOINTS
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MAKEPOINTS
 - wingdi/MAKEPOINTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - MAKEPOINTS
---

# MAKEPOINTS macro

## -syntax

```cpp
POINTS MAKEPOINTS(
    DWORD l
);
```

## -returns

Type: **POINTS**

The return value is a pointer to a <a href="/windows/win32/api/windef/ns-windef-points">POINTS</a> structure.


## -description

The <b>MAKEPOINTS</b> macro converts a value that contains the x- and y-coordinates of a point into a <a href="/windows/win32/api/windef/ns-windef-points">POINTS</a> structure.

## -parameters

### -param l

The coordinates of a point. The x-coordinate is in the low-order word, and the y-coordinate is in the high-order word.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getmessagepos">GetMessagePos</a>



<a href="/windows/desktop/gdi/rectangle-macros">Rectangle Macros</a>



<a href="/windows/desktop/gdi/rectangles">Rectangles Overview</a>
