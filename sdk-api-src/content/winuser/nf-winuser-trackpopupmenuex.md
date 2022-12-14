---
UID: NF:winuser.TrackPopupMenuEx
title: TrackPopupMenuEx function (winuser.h)
description: Displays a shortcut menu at the specified location and tracks the selection of items on the shortcut menu. The shortcut menu can appear anywhere on the screen.
helpviewer_keywords: ["TPM_BOTTOMALIGN","TPM_CENTERALIGN","TPM_HORIZONTAL","TPM_HORNEGANIMATION","TPM_HORPOSANIMATION","TPM_LEFTALIGN","TPM_LEFTBUTTON","TPM_NOANIMATION","TPM_NONOTIFY","TPM_RETURNCMD","TPM_RIGHTALIGN","TPM_RIGHTBUTTON","TPM_TOPALIGN","TPM_VCENTERALIGN","TPM_VERNEGANIMATION","TPM_VERPOSANIMATION","TPM_VERTICAL","TrackPopupMenuEx","TrackPopupMenuEx function [Menus and Other Resources]","_win32_TrackPopupMenuEx","_win32_trackpopupmenuex_cpp","menurc.trackpopupmenuex","winui._win32_trackpopupmenuex","winuser/TrackPopupMenuEx"]
old-location: menurc\trackpopupmenuex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\trackpopupmenuex.htm
ms.date: 12/05/2018
ms.keywords: TPM_BOTTOMALIGN, TPM_CENTERALIGN, TPM_HORIZONTAL, TPM_HORNEGANIMATION, TPM_HORPOSANIMATION, TPM_LEFTALIGN, TPM_LEFTBUTTON, TPM_NOANIMATION, TPM_NONOTIFY, TPM_RETURNCMD, TPM_RIGHTALIGN, TPM_RIGHTBUTTON, TPM_TOPALIGN, TPM_VCENTERALIGN, TPM_VERNEGANIMATION, TPM_VERPOSANIMATION, TPM_VERTICAL, TrackPopupMenuEx, TrackPopupMenuEx function [Menus and Other Resources], _win32_TrackPopupMenuEx, _win32_trackpopupmenuex_cpp, menurc.trackpopupmenuex, winui._win32_trackpopupmenuex, winuser/TrackPopupMenuEx
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
 - TrackPopupMenuEx
 - winuser/TrackPopupMenuEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - TrackPopupMenuEx
req.apiset: ext-ms-win-ntuser-menu-l1-1-1 (introduced in Windows 8.1)
---

# TrackPopupMenuEx function


## -description

Displays a shortcut menu at the specified location and tracks the selection of items on the shortcut menu. The shortcut menu can appear anywhere on the screen.

## -parameters

### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the shortcut menu to be displayed. This handle can be obtained by calling the <a href="/windows/desktop/api/winuser/nf-winuser-createpopupmenu">CreatePopupMenu</a> function to create a new shortcut menu or by calling the <a href="/windows/desktop/api/winuser/nf-winuser-getsubmenu">GetSubMenu</a> function to retrieve a handle to a submenu associated with an existing menu item.

### -param uFlags [in]

Type: <b>UINT</b>

Specifies function options. 


Use one of the following flags to specify how the function positions the shortcut menu horizontally. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TPM_CENTERALIGN"></a><a id="tpm_centeralign"></a><dl>
<dt><b>TPM_CENTERALIGN</b></dt>
<dt>0x0004L</dt>
</dl>
</td>
<td width="60%">
Centers the shortcut menu horizontally relative to the coordinate specified by the <i>x</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_LEFTALIGN"></a><a id="tpm_leftalign"></a><dl>
<dt><b>TPM_LEFTALIGN</b></dt>
<dt>0x0000L</dt>
</dl>
</td>
<td width="60%">
Positions the shortcut menu so that its left side is aligned with the coordinate specified by the <i>x</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_RIGHTALIGN"></a><a id="tpm_rightalign"></a><dl>
<dt><b>TPM_RIGHTALIGN</b></dt>
<dt>0x0008L</dt>
</dl>
</td>
<td width="60%">
Positions the shortcut menu so that its right side is aligned with the coordinate specified by the <i>x</i> parameter.

</td>
</tr>
</table>
 


Use one of the following flags to specify how the function positions the shortcut menu vertically.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TPM_BOTTOMALIGN"></a><a id="tpm_bottomalign"></a><dl>
<dt><b>TPM_BOTTOMALIGN</b></dt>
<dt>0x0020L</dt>
</dl>
</td>
<td width="60%">
Positions the shortcut menu so that its bottom side is aligned with the coordinate specified by the <i>y</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_TOPALIGN"></a><a id="tpm_topalign"></a><dl>
<dt><b>TPM_TOPALIGN</b></dt>
<dt>0x0000L</dt>
</dl>
</td>
<td width="60%">
Positions the shortcut menu so that its top side is aligned with the coordinate specified by the <i>y</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_VCENTERALIGN"></a><a id="tpm_vcenteralign"></a><dl>
<dt><b>TPM_VCENTERALIGN</b></dt>
<dt>0x0010L</dt>
</dl>
</td>
<td width="60%">
Centers the shortcut menu vertically relative to the coordinate specified by the <i>y</i> parameter.

</td>
</tr>
</table>
 


Use the following flags to control discovery of the user selection without having to set up a parent window for the menu. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TPM_NONOTIFY"></a><a id="tpm_nonotify"></a><dl>
<dt><b>TPM_NONOTIFY</b></dt>
<dt>0x0080L</dt>
</dl>
</td>
<td width="60%">
The function does not send notification messages when the user clicks a menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_RETURNCMD"></a><a id="tpm_returncmd"></a><dl>
<dt><b>TPM_RETURNCMD</b></dt>
<dt>0x0100L</dt>
</dl>
</td>
<td width="60%">
The function returns the menu item identifier of the user's selection in the return value.

</td>
</tr>
</table>
 


Use one of the following flags to specify which mouse button the shortcut menu tracks. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TPM_LEFTBUTTON"></a><a id="tpm_leftbutton"></a><dl>
<dt><b>TPM_LEFTBUTTON</b></dt>
<dt>0x0000L</dt>
</dl>
</td>
<td width="60%">
The user can select menu items with only the left mouse button.

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_RIGHTBUTTON"></a><a id="tpm_rightbutton"></a><dl>
<dt><b>TPM_RIGHTBUTTON</b></dt>
<dt>0x0002L</dt>
</dl>
</td>
<td width="60%">
The user can select menu items with both the left and right mouse buttons.

</td>
</tr>
</table>
 


Use any reasonable combination of the following flags to modify the animation of a menu. For example, by selecting a horizontal and a vertical flag, you can achieve diagonal animation. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TPM_HORNEGANIMATION"></a><a id="tpm_horneganimation"></a><dl>
<dt><b>TPM_HORNEGANIMATION</b></dt>
<dt>0x0800L</dt>
</dl>
</td>
<td width="60%">
Animates the menu from right to left.

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_HORPOSANIMATION"></a><a id="tpm_horposanimation"></a><dl>
<dt><b>TPM_HORPOSANIMATION</b></dt>
<dt>0x0400L</dt>
</dl>
</td>
<td width="60%">
Animates the menu from left to right.

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_NOANIMATION"></a><a id="tpm_noanimation"></a><dl>
<dt><b>TPM_NOANIMATION</b></dt>
<dt>0x4000L</dt>
</dl>
</td>
<td width="60%">
Displays menu without animation.

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_VERNEGANIMATION"></a><a id="tpm_verneganimation"></a><dl>
<dt><b>TPM_VERNEGANIMATION</b></dt>
<dt>0x2000L</dt>
</dl>
</td>
<td width="60%">
Animates the menu from bottom to top.

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_VERPOSANIMATION"></a><a id="tpm_verposanimation"></a><dl>
<dt><b>TPM_VERPOSANIMATION</b></dt>
<dt>0x1000L</dt>
</dl>
</td>
<td width="60%">
Animates the menu from top to bottom.

</td>
</tr>
</table>
 

For any animation to occur, the <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function must set <b>SPI_SETMENUANIMATION</b>. Also, all the <b>TPM_*ANIMATION</b> flags, except <b>TPM_NOANIMATION</b>, are ignored if menu fade animation is on. For more information, see the <b>SPI_GETMENUFADE</b> flag in <b>SystemParametersInfo</b>. 

 Use the <b>TPM_RECURSE</b> flag to display a menu when another menu is already displayed. This is intended to support context menus within a menu. 

Use one of the following flags to specify whether to accommodate horizontal or vertical alignment. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TPM_HORIZONTAL"></a><a id="tpm_horizontal"></a><dl>
<dt><b>TPM_HORIZONTAL</b></dt>
<dt>0x0000L</dt>
</dl>
</td>
<td width="60%">
If the menu cannot be shown at the specified location without overlapping the excluded rectangle, the system tries to accommodate the requested horizontal alignment before the requested vertical alignment.

</td>
</tr>
<tr>
<td width="40%"><a id="TPM_VERTICAL"></a><a id="tpm_vertical"></a><dl>
<dt><b>TPM_VERTICAL</b></dt>
<dt>0x0040L</dt>
</dl>
</td>
<td width="60%">
If the menu cannot be shown at the specified location without overlapping the excluded rectangle, the system tries to accommodate the requested vertical alignment before the requested horizontal alignment.

</td>
</tr>
</table>
 

The excluded rectangle is a portion of the screen that the menu should not overlap; it is specified by the <i>lptpm</i> parameter. 

 For right-to-left text layout, use <b>TPM_LAYOUTRTL</b>. By default, the text layout is left-to-right.

### -param x [in]

Type: <b>int</b>

The horizontal location of the shortcut menu, in screen coordinates.

### -param y [in]

Type: <b>int</b>

The vertical location of the shortcut menu, in screen coordinates.

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window that owns the shortcut menu. This window receives all messages from the menu. The window does not receive a <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> message from the menu until the function returns. If you specify TPM_NONOTIFY in the <i>fuFlags</i> parameter, the function does not send messages to the window identified by <i>hwnd</i>. However, you must still pass a window handle in <i>hwnd</i>. It can be any window handle from your application.

### -param lptpm [in, optional]

Type: <b>LPTPMPARAMS</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-tpmparams">TPMPARAMS</a> structure that specifies an area of the screen the menu should not overlap. This parameter can be <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

If you specify <b>TPM_RETURNCMD</b> in the <i>fuFlags</i> parameter, the return value is the menu-item identifier of the item that the user selected. If the user cancels the menu without making a selection, or if an error occurs, the return value is zero.

If you do not specify <b>TPM_RETURNCMD</b> in the <i>fuFlags</i> parameter, the return value is nonzero if the function succeeds and zero if it fails. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Call <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> with <b>SM_MENUDROPALIGNMENT</b> to determine the correct horizontal alignment flag (<b>TPM_LEFTALIGN</b> or <b>TPM_RIGHTALIGN</b>) and/or horizontal animation direction flag (<b>TPM_HORPOSANIMATION</b> or <b>TPM_HORNEGANIMATION</b>) to pass to <a href="/windows/desktop/api/winuser/nf-winuser-trackpopupmenu">TrackPopupMenu</a> or <b>TrackPopupMenuEx</b>. This is essential for creating an optimal user experience, especially when developing Microsoft Tablet PC applications.

To display a context menu for a notification icon, the current window must be the foreground window before the application calls <a href="/windows/desktop/api/winuser/nf-winuser-trackpopupmenu">TrackPopupMenu</a> or <b>TrackPopupMenuEx</b>. Otherwise, the menu will not disappear when the user clicks outside of the menu or the window that created the menu (if it is visible). If the current window is a child window, you must set the (top-level) parent window as the foreground window.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createpopupmenu">CreatePopupMenu</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getsubmenu">GetSubMenu</a>



<a href="/windows/desktop/menurc/menus">Menus</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/ns-winuser-tpmparams">TPMPARAMS</a>



<a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a>
