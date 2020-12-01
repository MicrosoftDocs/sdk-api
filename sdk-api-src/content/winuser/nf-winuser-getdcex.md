---
UID: NF:winuser.GetDCEx
title: GetDCEx function (winuser.h)
description: The GetDCEx function retrieves a handle to a device context (DC) for the client area of a specified window or for the entire screen.
helpviewer_keywords: ["DCX_CACHE","DCX_CLIPCHILDREN","DCX_CLIPSIBLINGS","DCX_EXCLUDERGN","DCX_INTERSECTRGN","DCX_INTERSECTUPDATE","DCX_LOCKWINDOWUPDATE","DCX_NORESETATTRS","DCX_PARENTCLIP","DCX_VALIDATE","DCX_WINDOW","GetDCEx","GetDCEx function [Windows GDI]","_win32_GetDCEx","gdi.getdcex","winuser/GetDCEx"]
old-location: gdi\getdcex.htm
tech.root: gdi
ms.assetid: 590cf928-0ad6-43f8-97e9-1dafbcfa9f49
ms.date: 12/05/2018
ms.keywords: DCX_CACHE, DCX_CLIPCHILDREN, DCX_CLIPSIBLINGS, DCX_EXCLUDERGN, DCX_INTERSECTRGN, DCX_INTERSECTUPDATE, DCX_LOCKWINDOWUPDATE, DCX_NORESETATTRS, DCX_PARENTCLIP, DCX_VALIDATE, DCX_WINDOW, GetDCEx, GetDCEx function [Windows GDI], _win32_GetDCEx, gdi.getdcex, winuser/GetDCEx
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
 - GetDCEx
 - winuser/GetDCEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-RTCore-NTUser-DC-Access-L1-1-1.dll
 - MinUser.dll
api_name:
 - GetDCEx
---

# GetDCEx function


## -description

The <b>GetDCEx</b> function retrieves a handle to a device context (DC) for the client area of a specified window or for the entire screen. You can use the returned handle in subsequent GDI functions to draw in the DC. The device context is an opaque data structure, whose values are used internally by GDI.

This function is an extension to the <a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a> function, which gives an application more control over how and whether clipping occurs in the client area.

## -parameters

### -param hWnd [in]

A handle to the window whose DC is to be retrieved. If this value is <b>NULL</b>, <b>GetDCEx</b> retrieves the DC for the entire screen.

### -param hrgnClip [in]

A clipping region that may be combined with the visible region of the DC. If the value of <i>flags</i> is DCX_INTERSECTRGN or DCX_EXCLUDERGN, then the operating system assumes ownership of the region and will automatically delete it when it is no longer needed. In this case, the application should not use or delete the region after a successful call to <b>GetDCEx</b>.

### -param flags [in]

Specifies how the DC is created. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DCX_WINDOW"></a><a id="dcx_window"></a><dl>
<dt><b>DCX_WINDOW</b></dt>
</dl>
</td>
<td width="60%">
Returns a DC that corresponds to the window rectangle rather than the client rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="DCX_CACHE"></a><a id="dcx_cache"></a><dl>
<dt><b>DCX_CACHE</b></dt>
</dl>
</td>
<td width="60%">
Returns a DC from the cache, rather than the OWNDC or CLASSDC window. Essentially overrides CS_OWNDC and CS_CLASSDC.

</td>
</tr>
<tr>
<td width="40%"><a id="DCX_PARENTCLIP"></a><a id="dcx_parentclip"></a><dl>
<dt><b>DCX_PARENTCLIP</b></dt>
</dl>
</td>
<td width="60%">
Uses the visible region of the parent window. The parent's WS_CLIPCHILDREN and CS_PARENTDC style bits are ignored. The origin is set to the upper-left corner of the window identified by <i>hWnd</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="DCX_CLIPSIBLINGS"></a><a id="dcx_clipsiblings"></a><dl>
<dt><b>DCX_CLIPSIBLINGS</b></dt>
</dl>
</td>
<td width="60%">
Excludes the visible regions of all sibling windows above the window identified by <i>hWnd</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="DCX_CLIPCHILDREN"></a><a id="dcx_clipchildren"></a><dl>
<dt><b>DCX_CLIPCHILDREN</b></dt>
</dl>
</td>
<td width="60%">
Excludes the visible regions of all child windows below the window identified by <i>hWnd</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="DCX_NORESETATTRS"></a><a id="dcx_noresetattrs"></a><dl>
<dt><b>DCX_NORESETATTRS</b></dt>
</dl>
</td>
<td width="60%">
This flag is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="DCX_LOCKWINDOWUPDATE"></a><a id="dcx_lockwindowupdate"></a><dl>
<dt><b>DCX_LOCKWINDOWUPDATE</b></dt>
</dl>
</td>
<td width="60%">
Allows drawing even if there is a <a href="/windows/desktop/api/winuser/nf-winuser-lockwindowupdate">LockWindowUpdate</a> call in effect that would otherwise exclude this window. Used for drawing during tracking.

</td>
</tr>
<tr>
<td width="40%"><a id="DCX_EXCLUDERGN"></a><a id="dcx_excludergn"></a><dl>
<dt><b>DCX_EXCLUDERGN</b></dt>
</dl>
</td>
<td width="60%">
The clipping region identified by <i>hrgnClip</i> is excluded from the visible region of the returned DC.

</td>
</tr>
<tr>
<td width="40%"><a id="DCX_INTERSECTRGN"></a><a id="dcx_intersectrgn"></a><dl>
<dt><b>DCX_INTERSECTRGN</b></dt>
</dl>
</td>
<td width="60%">
The clipping region identified by <i>hrgnClip</i> is intersected with the visible region of the returned DC.

</td>
</tr>
<tr>
<td width="40%"><a id="DCX_INTERSECTUPDATE"></a><a id="dcx_intersectupdate"></a><dl>
<dt><b>DCX_INTERSECTUPDATE</b></dt>
</dl>
</td>
<td width="60%">
Reserved; do not use.

</td>
</tr>
<tr>
<td width="40%"><a id="DCX_VALIDATE"></a><a id="dcx_validate"></a><dl>
<dt><b>DCX_VALIDATE</b></dt>
</dl>
</td>
<td width="60%">
Reserved; do not use.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is the handle to the DC for the specified window.

If the function fails, the return value is <b>NULL</b>. An invalid value for the <i>hWnd</i> parameter will cause the function to fail.

## -remarks

Unless the display DC belongs to a window class, the <a href="/windows/desktop/api/winuser/nf-winuser-releasedc">ReleaseDC</a> function must be called to release the DC after painting. Also, <b>ReleaseDC</b> must be called from the same thread that called <b>GetDCEx</b>. The number of DCs is limited only by available memory.

The function returns a handle to a DC that belongs to the window's class if CS_CLASSDC, CS_OWNDC or CS_PARENTDC was specified as a style in the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a> structure when the class was registered.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowdc">GetWindowDC</a>



<a href="/windows/desktop/api/winuser/nf-winuser-releasedc">ReleaseDC</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a>