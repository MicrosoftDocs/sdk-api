---
UID: NS:winuser.tagMOUSEKEYS
title: MOUSEKEYS (winuser.h)
description: Contains information about the MouseKeys accessibility feature.
helpviewer_keywords: ["*LPMOUSEKEYS","LPMOUSEKEYS","LPMOUSEKEYS structure pointer [Windows Accessibility]","MKF_AVAILABLE","MKF_CONFIRMHOTKEY","MKF_HOTKEYACTIVE","MKF_HOTKEYSOUND","MKF_INDICATOR","MKF_LEFTBUTTONDOWN","MKF_LEFTBUTTONSEL","MKF_MODIFIERS","MKF_MOUSEKEYSON","MKF_MOUSEMODE","MKF_REPLACENUMBERS","MKF_RIGHTBUTTONDOWN","MKF_RIGHTBUTTONSEL","MOUSEKEYS","MOUSEKEYS structure [Windows Accessibility]","_win32_MOUSEKEYS_str","msaa.mousekeys","tagMOUSEKEYS","winauto.mousekeys","winuser/LPMOUSEKEYS","winuser/MOUSEKEYS"]
old-location: winauto\mousekeys.htm
tech.root: WinAuto
ms.assetid: 437e448f-9eb3-4dfb-b1e8-61fceb904954
ms.date: 12/05/2018
ms.keywords: '*LPMOUSEKEYS, LPMOUSEKEYS, LPMOUSEKEYS structure pointer [Windows Accessibility], MKF_AVAILABLE, MKF_CONFIRMHOTKEY, MKF_HOTKEYACTIVE, MKF_HOTKEYSOUND, MKF_INDICATOR, MKF_LEFTBUTTONDOWN, MKF_LEFTBUTTONSEL, MKF_MODIFIERS, MKF_MOUSEKEYSON, MKF_MOUSEMODE, MKF_REPLACENUMBERS, MKF_RIGHTBUTTONDOWN, MKF_RIGHTBUTTONSEL, MOUSEKEYS, MOUSEKEYS structure [Windows Accessibility], _win32_MOUSEKEYS_str, msaa.mousekeys, tagMOUSEKEYS, winauto.mousekeys, winuser/LPMOUSEKEYS, winuser/MOUSEKEYS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MOUSEKEYS, *LPMOUSEKEYS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMOUSEKEYS
 - winuser/tagMOUSEKEYS
 - LPMOUSEKEYS
 - winuser/LPMOUSEKEYS
 - MOUSEKEYS
 - winuser/MOUSEKEYS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - MOUSEKEYS
---

# MOUSEKEYS structure


## -description

Contains information about the MouseKeys accessibility feature. When the MouseKeys feature is active, the user can use the numeric keypad to control the mouse pointer, and to click, double-click, drag, and drop. By pressing NUMLOCK, the user can toggle the numeric keypad between mouse control mode and normal operation.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the size, in bytes, of this structure.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>


A set of bit-flags that specify properties of the FilterKeys feature. The following bit-flag values are defined:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MKF_AVAILABLE"></a><a id="mkf_available"></a><dl>
<dt><b>MKF_AVAILABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the MouseKeys feature is available.

</td>
</tr>
<tr>
<td width="40%"><a id="MKF_CONFIRMHOTKEY"></a><a id="mkf_confirmhotkey"></a><dl>
<dt><b>MKF_CONFIRMHOTKEY</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> A confirmation dialog box appears when the MouseKeys feature is activated by using the hot key.

</td>
</tr>
<tr>
<td width="40%"><a id="MKF_HOTKEYACTIVE"></a><a id="mkf_hotkeyactive"></a><dl>
<dt><b>MKF_HOTKEYACTIVE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the user can turn the MouseKeys feature on and off by using the hot key, which is LEFT ALT+LEFT SHIFT+NUM LOCK.

</td>
</tr>
<tr>
<td width="40%"><a id="MKF_HOTKEYSOUND"></a><a id="mkf_hotkeysound"></a><dl>
<dt><b>MKF_HOTKEYSOUND</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the system plays a siren sound when the user turns the MouseKeys feature on or off by using the hot key.

</td>
</tr>
<tr>
<td width="40%"><a id="MKF_INDICATOR"></a><a id="mkf_indicator"></a><dl>
<dt><b>MKF_INDICATOR</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> A visual indicator is displayed when the MouseKeys feature is on.

</td>
</tr>
<tr>
<td width="40%"><a id="MKF_LEFTBUTTONDOWN"></a><a id="mkf_leftbuttondown"></a><dl>
<dt><b>MKF_LEFTBUTTONDOWN</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> The left button is in the "down" state.

</td>
</tr>
<tr>
<td width="40%"><a id="MKF_LEFTBUTTONSEL"></a><a id="mkf_leftbuttonsel"></a><dl>
<dt><b>MKF_LEFTBUTTONSEL</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> The user has selected the left button for mouse-button actions.

</td>
</tr>
<tr>
<td width="40%"><a id="MKF_MODIFIERS"></a><a id="mkf_modifiers"></a><dl>
<dt><b>MKF_MODIFIERS</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> The CTRL key increases cursor speed by the value specified by the <b>iCtrlSpeed</b> member, and the SHIFT key causes the cursor to delay briefly after moving a single pixel, allowing fine positioning of the cursor. If this value is not specified, the CTRL and SHIFT keys are ignored while the user moves the mouse cursor using the arrow keys.

</td>
</tr>
<tr>
<td width="40%"><a id="MKF_MOUSEKEYSON"></a><a id="mkf_mousekeyson"></a><dl>
<dt><b>MKF_MOUSEKEYSON</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the MouseKeys feature is on.

</td>
</tr>
<tr>
<td width="40%"><a id="MKF_MOUSEMODE"></a><a id="mkf_mousemode"></a><dl>
<dt><b>MKF_MOUSEMODE</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> The system is processing numeric keypad input as mouse commands.

</td>
</tr>
<tr>
<td width="40%"><a id="MKF_REPLACENUMBERS"></a><a id="mkf_replacenumbers"></a><dl>
<dt><b>MKF_REPLACENUMBERS</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> The numeric keypad moves the mouse when the NUM LOCK key is on. If this flag is not specified, the numeric keypad moves the mouse cursor when the NUM LOCK key is off.

</td>
</tr>
<tr>
<td width="40%"><a id="MKF_RIGHTBUTTONDOWN"></a><a id="mkf_rightbuttondown"></a><dl>
<dt><b>MKF_RIGHTBUTTONDOWN</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> The right button is in the "down" state.

</td>
</tr>
<tr>
<td width="40%"><a id="MKF_RIGHTBUTTONSEL"></a><a id="mkf_rightbuttonsel"></a><dl>
<dt><b>MKF_RIGHTBUTTONSEL</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> The user has selected the right button for mouse-button actions.

</td>
</tr>
</table>

### -field iMaxSpeed

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the maximum speed the mouse cursor attains when an arrow key is held down.

<b>Windows 95/98:</b> Range checking is not performed.

<b>Windows NT/2000:</b> Valid values are from 10 to 360.

### -field iTimeToMaxSpeed

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the length of time, in milliseconds, that it takes for the mouse cursor to reach maximum speed when an arrow key is held down. Valid values are from 1000 to 5000.

### -field iCtrlSpeed

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the multiplier to apply to the mouse cursor speed when the user holds down the CTRL key while using the arrow keys to move the cursor. this value is ignored if MKF_MODIFIERS is not set.

### -field dwReserved1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

This member is reserved for future use. It must be set to zero.

### -field dwReserved2

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

This member is reserved for future use. It must be set to zero.

## -remarks

An application uses a <b>MOUSEKEYS</b> structure when calling the <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function with the <i>uiAction</i> parameter set to the <b>SPI_GETMOUSEKEYS</b> or <b>SPI_SETMOUSEKEYS</b> value. When using <b>SPI_GETMOUSEKEYS</b>, an application must specify the <b>cbSize</b> member of the <b>MOUSEKEYS</b> structure; the <b>SystemParametersInfo</b> function fills the remaining members. An application must specify all structure members when using the <b>SPI_SETMOUSEKEYS</b> value.

If you call <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> with the <b>SPI_SETMOUSEKEYS</b> value, the following flags are ignored:

<ul>
<li><b>MKF_LEFTBUTTONDOWN</b></li>
<li><b>MKF_LEFTBUTTONSEL</b></li>
<li><b>MKF_MOUSEMODE</b></li>
<li><b>MKF_RIGHTBUTTONDOWN</b></li>
<li><b>MKF_RIGHTBUTTONSEL</b></li>
</ul>

## -see-also

<a href="/windows/desktop/WinAuto/accessibility-structures">Accessibility Structures</a>



<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>