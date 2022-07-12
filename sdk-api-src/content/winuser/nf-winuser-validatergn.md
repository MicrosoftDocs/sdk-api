---
UID: NF:winuser.ValidateRgn
title: ValidateRgn function (winuser.h)
description: The ValidateRgn function validates the client area within a region by removing the region from the current update region of the specified window.
helpviewer_keywords: ["ValidateRgn","ValidateRgn function [Windows GDI]","_win32_ValidateRgn","gdi.validatergn","winuser/ValidateRgn"]
old-location: gdi\validatergn.htm
tech.root: gdi
ms.assetid: 80fb1d4a-d9b1-4e67-b585-eee81893ed34
ms.date: 12/05/2018
ms.keywords: ValidateRgn, ValidateRgn function [Windows GDI], _win32_ValidateRgn, gdi.validatergn, winuser/ValidateRgn
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
 - ValidateRgn
 - winuser/ValidateRgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-0.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - ValidateRgn
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# ValidateRgn function


## -description

The <b>ValidateRgn</b> function validates the client area within a region by removing the region from the current update region of the specified window.

## -parameters

### -param hWnd [in]

Handle to the window whose update region is to be modified.

### -param hRgn [in]

Handle to a region that defines the area to be removed from the update region. If this parameter is <b>NULL</b>, the entire client area is removed.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The specified region must have been created by a region function. The region coordinates are assumed to be client coordinates.

The <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a> function automatically validates the entire client area. Neither the <a href="/windows/desktop/api/winuser/nf-winuser-validaterect">ValidateRect</a> nor <b>ValidateRgn</b> function should be called if a portion of the update region must be validated before the next <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message is generated.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<a href="/windows/desktop/api/winuser/nf-winuser-excludeupdatergn">ExcludeUpdateRgn</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidaterect">InvalidateRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidatergn">InvalidateRgn</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-validaterect">ValidateRect</a>



<a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a>
