---
UID: NS:winuser.tagTOGGLEKEYS
title: TOGGLEKEYS (winuser.h)
description: Contains information about the ToggleKeys accessibility feature.
helpviewer_keywords: ["*LPTOGGLEKEYS","LPTOGGLEKEYS","LPTOGGLEKEYS structure pointer [Windows Accessibility]","TKF_AVAILABLE","TKF_CONFIRMHOTKEY","TKF_HOTKEYACTIVE","TKF_HOTKEYSOUND","TKF_INDICATOR","TKF_TOGGLEKEYSON","TOGGLEKEYS","TOGGLEKEYS structure [Windows Accessibility]","_win32_TOGGLEKEYS_str","msaa.togglekeys","tagTOGGLEKEYS","winauto.togglekeys","winuser/LPTOGGLEKEYS","winuser/TOGGLEKEYS"]
old-location: winauto\togglekeys.htm
tech.root: WinAuto
ms.assetid: 85ebc8c2-ac0b-45f2-aee5-11ec4ba582b7
ms.date: 12/05/2018
ms.keywords: '*LPTOGGLEKEYS, LPTOGGLEKEYS, LPTOGGLEKEYS structure pointer [Windows Accessibility], TKF_AVAILABLE, TKF_CONFIRMHOTKEY, TKF_HOTKEYACTIVE, TKF_HOTKEYSOUND, TKF_INDICATOR, TKF_TOGGLEKEYSON, TOGGLEKEYS, TOGGLEKEYS structure [Windows Accessibility], _win32_TOGGLEKEYS_str, msaa.togglekeys, tagTOGGLEKEYS, winauto.togglekeys, winuser/LPTOGGLEKEYS, winuser/TOGGLEKEYS'
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
req.typenames: TOGGLEKEYS, *LPTOGGLEKEYS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTOGGLEKEYS
 - winuser/tagTOGGLEKEYS
 - LPTOGGLEKEYS
 - winuser/LPTOGGLEKEYS
 - TOGGLEKEYS
 - winuser/TOGGLEKEYS
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
 - TOGGLEKEYS
---

# TOGGLEKEYS structure


## -description

Contains information about the ToggleKeys accessibility feature. When the ToggleKeys feature is on, the computer emits a high-pitched tone whenever the user turns on the CAPS LOCK, NUM LOCK, or SCROLL LOCK key, and a low-pitched tone whenever the user turns off one of those keys.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the size, in bytes, of this structure.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>


A set of bit flags that specify properties of the ToggleKeys feature. The following bit flag values are defined:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TKF_AVAILABLE"></a><a id="tkf_available"></a><dl>
<dt><b>TKF_AVAILABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the ToggleKeys feature is available.

</td>
</tr>
<tr>
<td width="40%"><a id="TKF_CONFIRMHOTKEY"></a><a id="tkf_confirmhotkey"></a><dl>
<dt><b>TKF_CONFIRMHOTKEY</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> A confirmation dialog box appears when the ToggleKeys feature is activated by using the hot key.

</td>
</tr>
<tr>
<td width="40%"><a id="TKF_HOTKEYACTIVE"></a><a id="tkf_hotkeyactive"></a><dl>
<dt><b>TKF_HOTKEYACTIVE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the user can turn the ToggleKeys feature on and off by holding down the NUM LOCK key for eight seconds.

</td>
</tr>
<tr>
<td width="40%"><a id="TKF_HOTKEYSOUND"></a><a id="tkf_hotkeysound"></a><dl>
<dt><b>TKF_HOTKEYSOUND</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the system plays a siren sound when the user turns the ToggleKeys feature on or off by using the hot key.

</td>
</tr>
<tr>
<td width="40%"><a id="TKF_INDICATOR"></a><a id="tkf_indicator"></a><dl>
<dt><b>TKF_INDICATOR</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
This flag is not implemented.

</td>
</tr>
<tr>
<td width="40%"><a id="TKF_TOGGLEKEYSON"></a><a id="tkf_togglekeyson"></a><dl>
<dt><b>TKF_TOGGLEKEYSON</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the ToggleKeys feature is on.

</td>
</tr>
</table>

## -remarks

An application uses a <b>TOGGLEKEYS</b> structure when calling the <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function with the <i>uiAction</i> parameter set to <b>SPI_GETTOGGLEKEYS</b> or <b>SPI_SETTOGGLEKEYS</b>. When using SPI_GETTOGGLEKEYS, an application must specify the <b>cbSize</b> member of the <b>TOGGLEKEYS</b> structure; the <b>SystemParametersInfo</b> function fills the remaining members. An application must specify all structure members when using the <b>SPI_SETTOGGLEKEYS</b> value.

## -see-also

<a href="/windows/desktop/WinAuto/accessibility-structures">Accessibility Structures</a>



<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>