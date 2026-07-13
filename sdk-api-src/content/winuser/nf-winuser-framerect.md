---
UID: NF:winuser.FrameRect
title: FrameRect function (winuser.h)
description: The FrameRect function draws a border around the specified rectangle by using the specified brush. The width and height of the border are always one logical unit.
helpviewer_keywords: ["FrameRect","FrameRect function [Windows GDI]","_win32_FrameRect","gdi.framerect","winuser/FrameRect"]
old-location: gdi\framerect.htm
tech.root: gdi
ms.assetid: a1083cb5-5e6c-4134-badf-9fc5142d1453
ms.date: 12/05/2018
ms.keywords: FrameRect, FrameRect function [Windows GDI], _win32_FrameRect, gdi.framerect, winuser/FrameRect
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
 - FrameRect
 - winuser/FrameRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-gui-l1-1-1.dll
 - ext-ms-win-rtcore-ntuser-gui-l1-1-0.dll
 - ext-ms-win-ntuser-gui-l1-3-1.dll
 - user32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - FrameRect
req.apiset: ext-ms-win-ntuser-gui-l1-1-1 (introduced in Windows 8.1)
---

# FrameRect function


## -description

The <b>FrameRect</b> function draws a border around the specified rectangle by using the specified brush. The width and height of the border are always one logical unit.

## -parameters

### -param hDC [in]

A handle to the device context in which the border is drawn.

### -param lprc [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the logical coordinates of the upper-left and lower-right corners of the rectangle.

### -param hbr [in]

A handle to the brush used to draw the border.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The brush identified by the <i>hbr</i> parameter must have been created by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-createhatchbrush">CreateHatchBrush</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createpatternbrush">CreatePatternBrush</a>, or <a href="/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush">CreateSolidBrush</a> function, or retrieved by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-getstockobject">GetStockObject</a> function.

If the <b>bottom</b> member of the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure is less than the <b>top</b> member, or if the <b>right</b> member is less than the <b>left</b> member, the function does not draw the rectangle.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createhatchbrush">CreateHatchBrush
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpatternbrush">CreatePatternBrush
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush">CreateSolidBrush
      </a>



<a href="/windows/desktop/gdi/filled-shape-functions">Filled Shape Functions</a>



<a href="/windows/desktop/gdi/filled-shapes">Filled Shapes Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getstockobject">GetStockObject
      </a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT
      </a>
