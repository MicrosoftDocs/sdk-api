---
UID: NF:winuser.AnimateWindow
title: AnimateWindow function (winuser.h)
description: Enables you to produce special effects when showing or hiding windows. There are four types of animation:\_roll, slide, collapse or expand, and alpha-blended fade.
helpviewer_keywords: ["AW_ACTIVATE","AW_BLEND","AW_CENTER","AW_HIDE","AW_HOR_NEGATIVE","AW_HOR_POSITIVE","AW_SLIDE","AW_VER_NEGATIVE","AW_VER_POSITIVE","AnimateWindow","AnimateWindow function [Windows and Messages]","_win32_AnimateWindow","_win32_animatewindow_cpp","winmsg.animatewindow","winui._win32_animatewindow","winuser/AnimateWindow"]
old-location: winmsg\animatewindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\animatewindow.htm
ms.date: 12/05/2018
ms.keywords: AW_ACTIVATE, AW_BLEND, AW_CENTER, AW_HIDE, AW_HOR_NEGATIVE, AW_HOR_POSITIVE, AW_SLIDE, AW_VER_NEGATIVE, AW_VER_POSITIVE, AnimateWindow, AnimateWindow function [Windows and Messages], _win32_AnimateWindow, _win32_animatewindow_cpp, winmsg.animatewindow, winui._win32_animatewindow, winuser/AnimateWindow
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
 - AnimateWindow
 - winuser/AnimateWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - AnimateWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# AnimateWindow function


## -description

Enables you to produce special effects when showing or hiding windows. There are four types of animation: roll, slide, collapse or expand, and alpha-blended fade.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to animate. The calling thread must own this window.

### -param dwTime [in]

Type: <b>DWORD</b>

The time it takes to play the animation, in milliseconds. Typically, an animation takes 200 milliseconds to play.

### -param dwFlags [in]

Type: <b>DWORD</b>

The type of animation. This parameter can be one or more of the following values. Note that, by default, these flags take effect when showing a window. To take effect when hiding a window, use <b>AW_HIDE</b> and a logical OR operator with the appropriate flags. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AW_ACTIVATE"></a><a id="aw_activate"></a><dl>
<dt><b>AW_ACTIVATE</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Activates the window. Do not use this value with <b>AW_HIDE</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="AW_BLEND"></a><a id="aw_blend"></a><dl>
<dt><b>AW_BLEND</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Uses a fade effect. This flag can be used only if <i>hwnd</i> is a top-level window. 

</td>
</tr>
<tr>
<td width="40%"><a id="AW_CENTER"></a><a id="aw_center"></a><dl>
<dt><b>AW_CENTER</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Makes the window appear to collapse inward if <b>AW_HIDE</b> is used or expand outward if the <b>AW_HIDE</b> is not used. The various direction flags have no effect. 

</td>
</tr>
<tr>
<td width="40%"><a id="AW_HIDE"></a><a id="aw_hide"></a><dl>
<dt><b>AW_HIDE</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Hides the window. By default, the window is shown. 

</td>
</tr>
<tr>
<td width="40%"><a id="AW_HOR_POSITIVE"></a><a id="aw_hor_positive"></a><dl>
<dt><b>AW_HOR_POSITIVE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Animates the window from left to right. This flag can be used with roll or slide animation. It is ignored when used with <b>AW_CENTER</b> or <b>AW_BLEND</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="AW_HOR_NEGATIVE"></a><a id="aw_hor_negative"></a><dl>
<dt><b>AW_HOR_NEGATIVE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Animates the window from right to left. This flag can be used with roll or slide animation. It is ignored when used with <b>AW_CENTER</b> or <b>AW_BLEND</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="AW_SLIDE"></a><a id="aw_slide"></a><dl>
<dt><b>AW_SLIDE</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Uses slide animation. By default, roll animation is used. This flag is ignored when used with <b>AW_CENTER</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="AW_VER_POSITIVE"></a><a id="aw_ver_positive"></a><dl>
<dt><b>AW_VER_POSITIVE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Animates the window from top to bottom. This flag can be used with roll or slide animation. It is ignored when used with <b>AW_CENTER</b> or <b>AW_BLEND</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="AW_VER_NEGATIVE"></a><a id="aw_ver_negative"></a><dl>
<dt><b>AW_VER_NEGATIVE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Animates the window from bottom to top. This flag can be used with roll or slide animation. It is ignored when used with <b>AW_CENTER</b> or <b>AW_BLEND</b>. 

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. The function will fail in the following situations: 

<ul>
<li>If the window is already visible and you are trying to show the window.</li>
<li>If the window is already hidden and you are trying to hide the window.</li>
<li>If there is no direction specified for the slide or roll animation.</li>
<li>When trying to animate a child window with <b>AW_BLEND</b>. </li>
<li>If the thread does not own the window. Note that, in this case, <b>AnimateWindow</b> fails but <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_SUCCESS</b>.</li>
</ul>
To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

To show or hide a window without special effects, use <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>.

When using slide or roll animation, you must specify the direction. It can be either <b>AW_HOR_POSITIVE</b>, <b>AW_HOR_NEGATIVE</b>, AW_VER_POSITIVE, or AW_VER_NEGATIVE. 

You can combine <b>AW_HOR_POSITIVE</b> or <b>AW_HOR_NEGATIVE</b> with <b>AW_VER_POSITIVE</b> or <b>AW_VER_NEGATIVE</b> to animate a window diagonally. 

The window procedures for the window and its child windows should handle any <a href="/windows/desktop/gdi/wm-print">WM_PRINT</a> or <a href="/windows/desktop/gdi/wm-printclient">WM_PRINTCLIENT</a> messages. Dialog boxes, controls, and common controls already handle <b>WM_PRINTCLIENT</b>. The default window procedure already handles <b>WM_PRINT</b>. 

If a child window is displayed partially clipped, when it is animated it will have holes where it is clipped. 

<b>AnimateWindow</b> supports RTL windows.

Avoid animating a window that has a drop shadow because it produces visually distracting, jerky animations.

## -see-also

<b>Conceptual</b>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a>



<a href="/windows/desktop/gdi/wm-print">WM_PRINT</a>



<a href="/windows/desktop/gdi/wm-printclient">WM_PRINTCLIENT</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
