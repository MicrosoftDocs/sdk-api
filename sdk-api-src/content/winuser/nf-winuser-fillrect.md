---
UID: NF:winuser.FillRect
title: FillRect function (winuser.h)
description: The FillRect function fills a rectangle by using the specified brush. This function includes the left and top borders, but excludes the right and bottom borders of the rectangle.
helpviewer_keywords: ["FillRect","FillRect function [Windows GDI]","_win32_FillRect","gdi.fillrect","winuser/FillRect"]
old-location: gdi\fillrect.htm
tech.root: gdi
ms.assetid: 98ab34da-ea07-4446-a62e-509c849d95f9
ms.date: 12/05/2018
ms.keywords: FillRect, FillRect function [Windows GDI], _win32_FillRect, gdi.fillrect, winuser/FillRect
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
 - FillRect
 - winuser/FillRect
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
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - FillRect
req.apiset: ext-ms-win-ntuser-gui-l1-1-0 (introduced in Windows 8)
---

# FillRect function


## -description

The <b>FillRect</b> function fills a rectangle by using the specified brush. This function includes the left and top borders, but excludes the right and bottom borders of the rectangle.

## -parameters

### -param hDC [in]

A handle to the device context.

### -param lprc [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the logical coordinates of the rectangle to be filled.

### -param hbr [in]

A handle to the brush used to fill the rectangle.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The brush identified by the <i>hbr</i> parameter may be either a handle to a logical brush or a color value. If specifying a handle to a logical brush, call one of the following functions to obtain the handle: <a href="/windows/desktop/api/wingdi/nf-wingdi-createhatchbrush">CreateHatchBrush</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createpatternbrush">CreatePatternBrush</a>, or <a href="/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush">CreateSolidBrush</a>. Additionally, you may retrieve a handle to one of the stock brushes by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-getstockobject">GetStockObject</a> function. If specifying a color value for the <i>hbr</i> parameter, it must be one of the standard system colors (the value 1 must be added to the chosen color). For example:


```cpp

FillRect(hdc, &rect, (HBRUSH) (COLOR_WINDOW+1));

```


For a list of all the standard system colors, see <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a>.

When filling the specified rectangle, <b>FillRect</b> does not include the rectangle's right and bottom sides. GDI fills a rectangle up to, but not including, the right column and bottom row, regardless of the current mapping mode.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-rectangles">Using Rectangles</a>.

<div class="code"></div>

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
