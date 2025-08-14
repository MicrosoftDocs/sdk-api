---
UID: NF:winuser.DrawAnimatedRects
title: DrawAnimatedRects function (winuser.h)
description: Animates the caption of a window to indicate the opening of an icon or the minimizing or maximizing of a window.
helpviewer_keywords: ["DrawAnimatedRects","DrawAnimatedRects function [Windows GDI]","_win32_DrawAnimatedRects","gdi.drawanimatedrects","winuser/DrawAnimatedRects"]
old-location: gdi\drawanimatedrects.htm
tech.root: gdi
ms.assetid: 54a9234a-0056-4cfe-9158-86635dc31bc6
ms.date: 12/05/2018
ms.keywords: DrawAnimatedRects, DrawAnimatedRects function [Windows GDI], _win32_DrawAnimatedRects, gdi.drawanimatedrects, winuser/DrawAnimatedRects
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawAnimatedRects
 - winuser/DrawAnimatedRects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - ext-ms-win-ntuser-misc-l1-5-1.dll
 - ext-ms-win-ntuser-misc-l1-5-0.dll
 - ext-ms-win-ntuser-misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-2-0.dll
 - ext-ms-win-ntuser-misc-l1-1-0.dll
 - user32.dll
api_name:
 - DrawAnimatedRects
---

# DrawAnimatedRects function


## -description

Animates the caption of a window to indicate the opening of an icon or the minimizing or maximizing of a window.

## -parameters

### -param hwnd [in]

A handle to the window whose caption should be animated on the screen. The animation will be clipped to the parent of this window.

### -param idAni [in]

The type of animation. This must be IDANI_CAPTION. With the IDANI_CAPTION animation type, the window caption will animate from the position specified by lprcFrom to the position specified by lprcTo. The effect is similar to minimizing or maximizing a window.

### -param lprcFrom

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure specifying the location and size of the icon or minimized window. Coordinates are relative to the clipping window <i>hwnd</i>.

### -param lprcTo

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure specifying the location and size of the restored window. Coordinates are relative to the clipping window <i>hwnd</i>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>