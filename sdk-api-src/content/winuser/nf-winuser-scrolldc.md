---
UID: NF:winuser.ScrollDC
title: ScrollDC function (winuser.h)
description: The ScrollDC function scrolls a rectangle of bits horizontally and vertically.
helpviewer_keywords: ["ScrollDC","ScrollDC function [Windows Controls]","_win32_ScrollDC","_win32_ScrollDC_cpp","controls.ScrollDC","controls._win32_ScrollDC","winuser/ScrollDC"]
old-location: controls\ScrollDC.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\scrolldc.htm
ms.date: 12/05/2018
ms.keywords: ScrollDC, ScrollDC function [Windows Controls], _win32_ScrollDC, _win32_ScrollDC_cpp, controls.ScrollDC, controls._win32_ScrollDC, winuser/ScrollDC
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ScrollDC
 - winuser/ScrollDC
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
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - ScrollDC
req.apiset: ext-ms-win-ntuser-misc-l1-5-0 (introduced in Windows 10, version 10.0.10240)
---

# ScrollDC function


## -description

The <b>ScrollDC</b> function scrolls a rectangle of bits horizontally and vertically.

## -parameters

### -param hDC [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

Handle to the device context that contains the bits to be scrolled.

### -param dx [in]

Type: <b>int</b>

Specifies the amount, in device units, of horizontal scrolling. This parameter must be a negative value to scroll to the left.

### -param dy [in]

Type: <b>int</b>

Specifies the amount, in device units, of vertical scrolling. This parameter must be a negative value to scroll up.

### -param lprcScroll [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the coordinates of the bits to be scrolled. The only bits affected by the scroll operation are bits in the intersection of this rectangle and the rectangle specified by 
					<i>lprcClip</i>. If 
					<i>lprcScroll</i> is <b>NULL</b>, the entire client area is used.

### -param lprcClip [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the coordinates of the clipping rectangle. The only bits that will be painted are the bits that remain inside this rectangle after the scroll operation has been completed. If 
					<i>lprcClip</i> is <b>NULL</b>, the entire client area is used.

### -param hrgnUpdate [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRGN</a></b>

Handle to the region uncovered by the scrolling process. <b>ScrollDC</b> defines this region; it is not necessarily a rectangle.

### -param lprcUpdate [out]

Type: <b>LPRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the coordinates of the rectangle bounding the scrolling update region. This is the largest rectangular area that requires repainting. When the function returns, the values in the structure are in client coordinates, regardless of the mapping mode for the specified device context. This allows applications to use the update region in a call to the <a href="/windows/desktop/api/winuser/nf-winuser-invalidatergn">InvalidateRgn</a> function, if required.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the 
				<i>lprcUpdate</i> parameter is <b>NULL</b>, the system does not compute the update rectangle. If both the 
				<i>hrgnUpdate</i> and 
				<i>lprcUpdate</i> parameters are <b>NULL</b>, the system does not compute the update region. If 
				<i>hrgnUpdate</i> is not <b>NULL</b>, the system proceeds as though it contains a valid handle to the region uncovered by the scrolling process (defined by <b>ScrollDC</b>). 

When you must scroll the entire client area of a window, use the <a href="/windows/desktop/api/winuser/nf-winuser-scrollwindowex">ScrollWindowEx</a> function.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-invalidatergn">InvalidateRgn</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-scrollwindowex">ScrollWindowEx</a>
