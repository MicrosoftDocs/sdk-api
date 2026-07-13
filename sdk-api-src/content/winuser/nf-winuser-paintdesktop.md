---
UID: NF:winuser.PaintDesktop
title: PaintDesktop function (winuser.h)
description: The PaintDesktop function fills the clipping region in the specified device context with the desktop pattern or wallpaper. The function is provided primarily for shell desktops.
helpviewer_keywords: ["PaintDesktop","PaintDesktop function [Windows GDI]","_win32_PaintDesktop","gdi.paintdesktop","winuser/PaintDesktop"]
old-location: gdi\paintdesktop.htm
tech.root: gdi
ms.assetid: 738500d4-32f5-43cf-8d40-9ad201ca6d4b
ms.date: 12/05/2018
ms.keywords: PaintDesktop, PaintDesktop function [Windows GDI], _win32_PaintDesktop, gdi.paintdesktop, winuser/PaintDesktop
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
 - PaintDesktop
 - winuser/PaintDesktop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-draw-l1-1-2.dll
 - ext-ms-win-ntuser-draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-0.dll
 - user32.dll
api_name:
 - PaintDesktop
---

# PaintDesktop function


## -description

The <b>PaintDesktop</b> function fills the clipping region in the specified device context with the desktop pattern or wallpaper. The function is provided primarily for shell desktops.

## -parameters

### -param hdc [in]

Handle to the device context.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>