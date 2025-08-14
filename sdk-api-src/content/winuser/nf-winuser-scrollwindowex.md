---
UID: NF:winuser.ScrollWindowEx
title: ScrollWindowEx function (winuser.h)
description: The ScrollWindowEx function scrolls the contents of the specified window's client area.
helpviewer_keywords: ["SW_ERASE","SW_INVALIDATE","SW_SCROLLCHILDREN","SW_SMOOTHSCROLL","ScrollWindowEx","ScrollWindowEx function [Windows Controls]","_win32_ScrollWindowEx","_win32_ScrollWindowEx_cpp","controls.ScrollWindowEx","controls._win32_ScrollWindowEx","winuser/ScrollWindowEx"]
old-location: controls\ScrollWindowEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\scrollwindowex.htm
ms.date: 12/05/2018
ms.keywords: SW_ERASE, SW_INVALIDATE, SW_SCROLLCHILDREN, SW_SMOOTHSCROLL, ScrollWindowEx, ScrollWindowEx function [Windows Controls], _win32_ScrollWindowEx, _win32_ScrollWindowEx_cpp, controls.ScrollWindowEx, controls._win32_ScrollWindowEx, winuser/ScrollWindowEx
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
 - ScrollWindowEx
 - winuser/ScrollWindowEx
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
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - ScrollWindowEx
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# ScrollWindowEx function


## -description

The <b>ScrollWindowEx</b> function scrolls the contents of the specified window's client area.

## -parameters

### -param hWnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the window where the client area is to be scrolled.

### -param dx [in]

Type: <b>int</b>

Specifies the amount, in device units, of horizontal scrolling. This parameter must be a negative value to scroll to the left.

### -param dy [in]

Type: <b>int</b>

Specifies the amount, in device units, of vertical scrolling. This parameter must be a negative value to scroll up.

### -param prcScroll [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the portion of the client area to be scrolled. If this parameter is <b>NULL</b>, the entire client area is scrolled.

### -param prcClip [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the coordinates of the clipping rectangle. Only device bits within the clipping rectangle are affected. Bits scrolled from the outside of the rectangle to the inside are painted; bits scrolled from the inside of the rectangle to the outside are not painted. This parameter may be <b>NULL</b>.

### -param hrgnUpdate [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRGN</a></b>

Handle to the region that is modified to hold the region invalidated by scrolling. This parameter may be <b>NULL</b>.

### -param prcUpdate [out]

Type: <b>LPRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the boundaries of the rectangle invalidated by scrolling. This parameter may be <b>NULL</b>.

### -param flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies flags that control scrolling. This parameter can be a combination of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SW_ERASE"></a><a id="sw_erase"></a><dl>
<dt><b>SW_ERASE</b></dt>
</dl>
</td>
<td width="60%">
Erases the newly invalidated region by sending a 
						<a href="/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a> message to the window when specified with the SW_INVALIDATE flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_INVALIDATE"></a><a id="sw_invalidate"></a><dl>
<dt><b>SW_INVALIDATE</b></dt>
</dl>
</td>
<td width="60%">
Invalidates the region identified by the 
						<i>hrgnUpdate</i> parameter after scrolling.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SCROLLCHILDREN"></a><a id="sw_scrollchildren"></a><dl>
<dt><b>SW_SCROLLCHILDREN</b></dt>
</dl>
</td>
<td width="60%">
Scrolls all child windows that intersect the rectangle pointed to by the 
						<i>prcScroll</i> parameter. The child windows are scrolled by the number of pixels specified by the 
						<i>dx</i> and 
						<i>dy</i> parameters. The system sends a 
						<a href="/windows/desktop/winmsg/wm-move">WM_MOVE</a> message to all child windows that intersect the 
						<i>prcScroll</i> rectangle, even if they do not move.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SMOOTHSCROLL"></a><a id="sw_smoothscroll"></a><dl>
<dt><b>SW_SMOOTHSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Scrolls using smooth scrolling. Use the 
						<a href="/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)">HIWORD</a> portion of the 
						<i>flags</i> parameter to indicate how much time, in milliseconds, the smooth-scrolling operation should take.

</td>
</tr>
</table>

## -returns

Type: <b>int</b>

If the function succeeds, the return value is SIMPLEREGION (rectangular invalidated region), COMPLEXREGION (nonrectangular invalidated region; overlapping rectangles), or NULLREGION (no invalidated region). 

If the function fails, the return value is ERROR. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the SW_INVALIDATE and SW_ERASE flags are not specified, <b>ScrollWindowEx</b> does not invalidate the area that is scrolled from. If either of these flags is set, <b>ScrollWindowEx</b> invalidates this area. The area is not updated until the application calls the <a href="/windows/desktop/api/winuser/nf-winuser-updatewindow">UpdateWindow</a> function, calls the  <a href="/windows/desktop/api/winuser/nf-winuser-redrawwindow">RedrawWindow</a> function (specifying the RDW_UPDATENOW or RDW_ERASENOW flag), or retrieves the 
				<a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message from the application queue. 

If the window has the <a href="/windows/desktop/winmsg/window-styles">WS_CLIPCHILDREN</a> style, the returned areas specified by 
				<i>hrgnUpdate</i> and 
				<i>prcUpdate</i> represent the total area of the scrolled window that must be updated, including any areas in child windows that need updating. 

If the SW_SCROLLCHILDREN flag is specified, the system does not properly update the screen if part of a child window is scrolled. The part of the scrolled child window that lies outside the source rectangle is not erased and is not properly redrawn in its new destination. To move child windows that do not lie completely within the rectangle specified by 
				<i>prcScroll</i>, use the <a href="/windows/desktop/api/winuser/nf-winuser-deferwindowpos">DeferWindowPos</a> function. The cursor is repositioned if the SW_SCROLLCHILDREN flag is set and the caret rectangle intersects the scroll rectangle. 

All input and output coordinates (for 
				<i>prcScroll</i>, 
				<i>prcClip</i>, 
				<i>prcUpdate</i>, and 
				<i>hrgnUpdate</i>) are determined as client coordinates, regardless of whether the window has the <a href="/windows/desktop/winmsg/window-class-styles">CS_OWNDC</a> or <a href="/windows/desktop/winmsg/window-class-styles">CS_CLASSDC</a> class style. Use the 
				<a href="/windows/desktop/api/wingdi/nf-wingdi-lptodp">LPtoDP</a> and 
				<a href="/windows/desktop/api/wingdi/nf-wingdi-dptolp">DPtoLP</a> functions to convert to and from logical coordinates, if necessary. 


#### Examples

For an example, see <a href="/windows/desktop/Controls/using-scroll-bars">Scrolling Text with the WM_PAINT Message</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-dptolp">DPtoLP</a>



<a href="/windows/desktop/api/winuser/nf-winuser-deferwindowpos">DeferWindowPos</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-lptodp">LPtoDP</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/winuser/nf-winuser-redrawwindow">RedrawWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-updatewindow">UpdateWindow</a>
