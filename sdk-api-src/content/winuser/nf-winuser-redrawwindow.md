---
UID: NF:winuser.RedrawWindow
title: RedrawWindow function (winuser.h)
description: The RedrawWindow function updates the specified rectangle or region in a window's client area.
helpviewer_keywords: ["RDW_ALLCHILDREN","RDW_ERASE","RDW_ERASENOW","RDW_FRAME","RDW_INTERNALPAINT","RDW_INVALIDATE","RDW_NOCHILDREN","RDW_NOERASE","RDW_NOFRAME","RDW_NOINTERNALPAINT","RDW_UPDATENOW","RDW_VALIDATE","RedrawWindow","RedrawWindow function [Windows GDI]","_win32_RedrawWindow","gdi.redrawwindow","winuser/RedrawWindow"]
old-location: gdi\redrawwindow.htm
tech.root: gdi
ms.assetid: c6cb7f74-237e-4d3e-a852-894da36e990c
ms.date: 12/05/2018
ms.keywords: RDW_ALLCHILDREN, RDW_ERASE, RDW_ERASENOW, RDW_FRAME, RDW_INTERNALPAINT, RDW_INVALIDATE, RDW_NOCHILDREN, RDW_NOERASE, RDW_NOFRAME, RDW_NOINTERNALPAINT, RDW_UPDATENOW, RDW_VALIDATE, RedrawWindow, RedrawWindow function [Windows GDI], _win32_RedrawWindow, gdi.redrawwindow, winuser/RedrawWindow
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
 - RedrawWindow
 - winuser/RedrawWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - API-MS-Win-RTCore-NTUser-Draw-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-0.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Draw-Ext-L1-1-0.dll
api_name:
 - RedrawWindow
req.apiset: ext-ms-win-ntuser-draw-l1-1-0 (introduced in Windows 8)
---

# RedrawWindow function


## -description

The <b>RedrawWindow</b> function updates the specified rectangle or region in a window's client area.

## -parameters

### -param hWnd [in]

A handle to the window to be redrawn. If this parameter is <b>NULL</b>, the desktop window is updated.

### -param lprcUpdate [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the coordinates, in device units, of the update rectangle. This parameter is ignored if the <i>hrgnUpdate</i> parameter identifies a region.

### -param hrgnUpdate [in]

A handle to the update region. If both the <i>hrgnUpdate</i> and <i>lprcUpdate</i> parameters are <b>NULL</b>, the entire client area is added to the update region.

### -param flags [in]

One or more redraw flags. This parameter can be used to invalidate or validate a window, control repainting, and control which windows are affected by <b>RedrawWindow</b>.

The following flags are used to invalidate the window.

<table>
<tr>
<th>Flag (invalidation)</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="RDW_ERASE"></a><a id="rdw_erase"></a><dl>
<dt><b>RDW_ERASE</b></dt>
</dl>
</td>
<td width="60%">
Causes the window to receive a <a href="/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a> message when the window is repainted. The RDW_INVALIDATE flag must also be specified; otherwise, RDW_ERASE has no effect.

</td>
</tr>
<tr>
<td width="40%"><a id="RDW_FRAME"></a><a id="rdw_frame"></a><dl>
<dt><b>RDW_FRAME</b></dt>
</dl>
</td>
<td width="60%">
Causes any part of the nonclient area of the window that intersects the update region to receive a <a href="/windows/desktop/gdi/wm-ncpaint">WM_NCPAINT</a> message. The RDW_INVALIDATE flag must also be specified; otherwise, RDW_FRAME has no effect. The <b>WM_NCPAINT</b> message is typically not sent during the execution of <b>RedrawWindow</b> unless either RDW_UPDATENOW or RDW_ERASENOW is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="RDW_INTERNALPAINT"></a><a id="rdw_internalpaint"></a><dl>
<dt><b>RDW_INTERNALPAINT</b></dt>
</dl>
</td>
<td width="60%">
Causes a <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message to be posted to the window regardless of whether any portion of the window is invalid.

</td>
</tr>
<tr>
<td width="40%"><a id="RDW_INVALIDATE"></a><a id="rdw_invalidate"></a><dl>
<dt><b>RDW_INVALIDATE</b></dt>
</dl>
</td>
<td width="60%">
Invalidates <i>lprcUpdate</i> or <i>hrgnUpdate</i> (only one may be non-<b>NULL</b>). If both are <b>NULL</b>, the entire window is invalidated.

</td>
</tr>
</table>
 

The following flags are used to validate the window.

<table>
<tr>
<th>Flag (validation)</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="RDW_NOERASE"></a><a id="rdw_noerase"></a><dl>
<dt><b>RDW_NOERASE</b></dt>
</dl>
</td>
<td width="60%">
Suppresses any pending <a href="/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a> messages.

</td>
</tr>
<tr>
<td width="40%"><a id="RDW_NOFRAME"></a><a id="rdw_noframe"></a><dl>
<dt><b>RDW_NOFRAME</b></dt>
</dl>
</td>
<td width="60%">
Suppresses any pending <a href="/windows/desktop/gdi/wm-ncpaint">WM_NCPAINT</a> messages. This flag must be used with RDW_VALIDATE and is typically used with RDW_NOCHILDREN. RDW_NOFRAME should be used with care, as it could cause parts of a window to be painted improperly.

</td>
</tr>
<tr>
<td width="40%"><a id="RDW_NOINTERNALPAINT"></a><a id="rdw_nointernalpaint"></a><dl>
<dt><b>RDW_NOINTERNALPAINT</b></dt>
</dl>
</td>
<td width="60%">
Suppresses any pending internal <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> messages. This flag does not affect <b>WM_PAINT</b> messages resulting from a non-<b>NULL</b> update area.

</td>
</tr>
<tr>
<td width="40%"><a id="RDW_VALIDATE"></a><a id="rdw_validate"></a><dl>
<dt><b>RDW_VALIDATE</b></dt>
</dl>
</td>
<td width="60%">
Validates <i>lprcUpdate</i> or <i>hrgnUpdate</i> (only one may be non-<b>NULL</b>). If both are <b>NULL</b>, the entire window is validated. This flag does not affect internal <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> messages.

</td>
</tr>
</table>
 

The following flags control when repainting occurs. <b>RedrawWindow</b> will not repaint unless one of these flags is specified.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="RDW_ERASENOW"></a><a id="rdw_erasenow"></a><dl>
<dt><b>RDW_ERASENOW</b></dt>
</dl>
</td>
<td width="60%">
Causes the affected windows (as specified by the RDW_ALLCHILDREN and RDW_NOCHILDREN flags) to receive <a href="/windows/desktop/gdi/wm-ncpaint">WM_NCPAINT</a> and <a href="/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a> messages, if necessary, before the function returns. <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> messages are received at the ordinary time.

</td>
</tr>
<tr>
<td width="40%"><a id="RDW_UPDATENOW"></a><a id="rdw_updatenow"></a><dl>
<dt><b>RDW_UPDATENOW</b></dt>
</dl>
</td>
<td width="60%">
Causes the affected windows (as specified by the RDW_ALLCHILDREN and RDW_NOCHILDREN flags) to receive <a href="/windows/desktop/gdi/wm-ncpaint">WM_NCPAINT</a>, <a href="/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a>, and <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> messages, if necessary, before the function returns.

</td>
</tr>
</table>
 

By default, the windows affected by <b>RedrawWindow</b> depend on whether the specified window has the WS_CLIPCHILDREN style. Child windows that are not the WS_CLIPCHILDREN style are unaffected; non-WS_CLIPCHILDREN windows are recursively validated or invalidated until a WS_CLIPCHILDREN window is encountered. The following flags control which windows are affected by the <b>RedrawWindow</b> function.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="RDW_ALLCHILDREN"></a><a id="rdw_allchildren"></a><dl>
<dt><b>RDW_ALLCHILDREN</b></dt>
</dl>
</td>
<td width="60%">
Includes child windows, if any, in the repainting operation.

</td>
</tr>
<tr>
<td width="40%"><a id="RDW_NOCHILDREN"></a><a id="rdw_nochildren"></a><dl>
<dt><b>RDW_NOCHILDREN</b></dt>
</dl>
</td>
<td width="60%">
Excludes child windows, if any, from the repainting operation.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

When <b>RedrawWindow</b> is used to invalidate part of the desktop window, the desktop window does not receive a <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> message. To repaint the desktop, an application uses the RDW_ERASE flag to generate a <a href="/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a> message.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getupdaterect">GetUpdateRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getupdatergn">GetUpdateRgn</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidaterect">InvalidateRect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-invalidatergn">InvalidateRgn</a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/winuser/nf-winuser-updatewindow">UpdateWindow</a>
