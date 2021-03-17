---
UID: NF:wingdi.RectVisible
title: RectVisible function (wingdi.h)
description: The RectVisible function determines whether any part of the specified rectangle lies within the clipping region of a device context.
helpviewer_keywords: ["RectVisible","RectVisible function [Windows GDI]","_win32_RectVisible","gdi.rectvisible","wingdi/RectVisible"]
old-location: gdi\rectvisible.htm
tech.root: gdi
ms.assetid: 990e9b22-0ce3-42b8-a87e-32fd2f2bc2fb
ms.date: 12/05/2018
ms.keywords: RectVisible, RectVisible function [Windows GDI], _win32_RectVisible, gdi.rectvisible, wingdi/RectVisible
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
 - RectVisible
 - wingdi/RectVisible
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-clipping-l1-1-0.dll
 - GDI32Full.dll
api_name:
 - RectVisible
---

# RectVisible function


## -description

The <b>RectVisible</b> function determines whether any part of the specified rectangle lies within the clipping region of a device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lprect [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the logical coordinates of the specified rectangle.

## -returns

If the current transform does not have a rotation and the rectangle lies within the clipping region, the return value is <b>TRUE</b> (1).

If the current transform does not have a rotation and the rectangle does not lie within the clipping region, the return value is <b>FALSE</b> (0).

If the current transform has a rotation and the rectangle lies within the clipping region, the return value is 2.

If the current transform has a rotation and the rectangle does not lie within the clipping region, the return value is 1.

All other return values are considered error codes. If the any parameter is not valid, the return value is undefined.

## -see-also

<a href="/windows/desktop/gdi/clipping-functions">Clipping Functions</a>



<a href="/windows/desktop/gdi/clipping">Clipping Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgn">CreateRectRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-ptvisible">PtVisible</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectcliprgn">SelectClipRgn</a>