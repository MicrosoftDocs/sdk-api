---
UID: NS:winuser.tagSTICKYKEYS
title: STICKYKEYS (winuser.h)
description: Contains information about the StickyKeys accessibility feature.
helpviewer_keywords: ["*LPSTICKYKEYS","LPSTICKYKEYS","LPSTICKYKEYS structure pointer [Windows Accessibility]","SKF_AUDIBLEFEEDBACK","SKF_AVAILABLE","SKF_CONFIRMHOTKEY","SKF_HOTKEYACTIVE","SKF_HOTKEYSOUND","SKF_INDICATOR","SKF_LALTLATCHED","SKF_LALTLOCKED","SKF_LCTLLATCHED","SKF_LCTLLOCKED","SKF_LSHIFTLATCHED","SKF_LSHIFTLOCKED","SKF_LWINLATCHED","SKF_LWINLOCKED","SKF_RALTLATCHED","SKF_RALTLOCKED","SKF_RCTLLATCHED","SKF_RCTLLOCKED","SKF_RSHIFTLATCHED","SKF_RSHIFTLOCKED","SKF_RWINLATCHED","SKF_RWINLOCKED","SKF_STICKYKEYSON","SKF_TRISTATE","SKF_TWOKEYSOFF","STICKYKEYS","STICKYKEYS structure [Windows Accessibility]","_win32_STICKYKEYS_str","msaa.stickykeys","tagSTICKYKEYS","winauto.stickykeys","winuser/LPSTICKYKEYS","winuser/STICKYKEYS"]
old-location: winauto\stickykeys.htm
tech.root: WinAuto
ms.assetid: 92fedb82-fff5-447f-b240-5dba8bb2eaea
ms.date: 12/05/2018
ms.keywords: '*LPSTICKYKEYS, LPSTICKYKEYS, LPSTICKYKEYS structure pointer [Windows Accessibility], SKF_AUDIBLEFEEDBACK, SKF_AVAILABLE, SKF_CONFIRMHOTKEY, SKF_HOTKEYACTIVE, SKF_HOTKEYSOUND, SKF_INDICATOR, SKF_LALTLATCHED, SKF_LALTLOCKED, SKF_LCTLLATCHED, SKF_LCTLLOCKED, SKF_LSHIFTLATCHED, SKF_LSHIFTLOCKED, SKF_LWINLATCHED, SKF_LWINLOCKED, SKF_RALTLATCHED, SKF_RALTLOCKED, SKF_RCTLLATCHED, SKF_RCTLLOCKED, SKF_RSHIFTLATCHED, SKF_RSHIFTLOCKED, SKF_RWINLATCHED, SKF_RWINLOCKED, SKF_STICKYKEYSON, SKF_TRISTATE, SKF_TWOKEYSOFF, STICKYKEYS, STICKYKEYS structure [Windows Accessibility], _win32_STICKYKEYS_str, msaa.stickykeys, tagSTICKYKEYS, winauto.stickykeys, winuser/LPSTICKYKEYS, winuser/STICKYKEYS'
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
req.typenames: STICKYKEYS, *LPSTICKYKEYS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTICKYKEYS
 - winuser/tagSTICKYKEYS
 - LPSTICKYKEYS
 - winuser/LPSTICKYKEYS
 - STICKYKEYS
 - winuser/STICKYKEYS
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
 - STICKYKEYS
---

# STICKYKEYS structure


## -description

Contains information about the StickyKeys accessibility feature. When the StickyKeys feature is on, the user can press a modifier key (SHIFT, CTRL, or ALT) and then another key in sequence rather than at the same time, to enter shifted (modified) characters and other key combinations. Pressing a modifier key once <i>latches</i> the key down until the user presses a non-modifier key or clicks a mouse button. Pressing a modifier key twice <i>locks</i> the key until the user presses the key a third time.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the size, in bytes, of this structure.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>


A set of bit-flags that specify properties of the StickyKeys feature. The following bit-flag values are defined:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SKF_AUDIBLEFEEDBACK"></a><a id="skf_audiblefeedback"></a><dl>
<dt><b>SKF_AUDIBLEFEEDBACK</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the system plays a sound when the user latches, locks, or releases modifier keys using the StickyKeys feature.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_AVAILABLE"></a><a id="skf_available"></a><dl>
<dt><b>SKF_AVAILABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the StickyKeys feature is available.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_CONFIRMHOTKEY"></a><a id="skf_confirmhotkey"></a><dl>
<dt><b>SKF_CONFIRMHOTKEY</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> A confirmation dialog appears when the StickyKeys feature is activated by using the hot key.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_HOTKEYACTIVE"></a><a id="skf_hotkeyactive"></a><dl>
<dt><b>SKF_HOTKEYACTIVE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the user can turn the StickyKeys feature on and off by pressing the SHIFT key five times.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_HOTKEYSOUND"></a><a id="skf_hotkeysound"></a><dl>
<dt><b>SKF_HOTKEYSOUND</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the system plays a siren sound when the user turns the StickyKeys feature on or off by using the hot key.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_INDICATOR"></a><a id="skf_indicator"></a><dl>
<dt><b>SKF_INDICATOR</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> A visual indicator should be displayed when the StickyKeys feature is on.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_STICKYKEYSON"></a><a id="skf_stickykeyson"></a><dl>
<dt><b>SKF_STICKYKEYSON</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the StickyKeys feature is on.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_TRISTATE"></a><a id="skf_tristate"></a><dl>
<dt><b>SKF_TRISTATE</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
If this flag is set, pressing a modifier key twice in a row locks down the key until the user presses it a third time.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_TWOKEYSOFF"></a><a id="skf_twokeysoff"></a><dl>
<dt><b>SKF_TWOKEYSOFF</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
If this flag is set, releasing a modifier key that has been pressed in combination with any other key turns off the StickyKeys feature.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_LALTLATCHED"></a><a id="skf_laltlatched"></a><dl>
<dt><b>SKF_LALTLATCHED</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b>The left ALT key is latched.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_LCTLLATCHED"></a><a id="skf_lctllatched"></a><dl>
<dt><b>SKF_LCTLLATCHED</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The left CTRL key is latched.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_LSHIFTLATCHED"></a><a id="skf_lshiftlatched"></a><dl>
<dt><b>SKF_LSHIFTLATCHED</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The left SHIFT key is latched.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_RALTLATCHED"></a><a id="skf_raltlatched"></a><dl>
<dt><b>SKF_RALTLATCHED</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The right ALT key is latched.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_RCTLLATCHED"></a><a id="skf_rctllatched"></a><dl>
<dt><b>SKF_RCTLLATCHED</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The right CTRL key is latched.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_RSHIFTLATCHED"></a><a id="skf_rshiftlatched"></a><dl>
<dt><b>SKF_RSHIFTLATCHED</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The right SHIFT key is latched.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_LALTLOCKED"></a><a id="skf_laltlocked"></a><dl>
<dt><b>SKF_LALTLOCKED</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The left ALT key is locked.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_LCTLLOCKED"></a><a id="skf_lctllocked"></a><dl>
<dt><b>SKF_LCTLLOCKED</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The left CTRL key is locked.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_LSHIFTLOCKED"></a><a id="skf_lshiftlocked"></a><dl>
<dt><b>SKF_LSHIFTLOCKED</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The left SHIFT key is locked.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_RALTLOCKED"></a><a id="skf_raltlocked"></a><dl>
<dt><b>SKF_RALTLOCKED</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The right ALT key is locked.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_RCTLLOCKED"></a><a id="skf_rctllocked"></a><dl>
<dt><b>SKF_RCTLLOCKED</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The right CTRL key is locked.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_RSHIFTLOCKED"></a><a id="skf_rshiftlocked"></a><dl>
<dt><b>SKF_RSHIFTLOCKED</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The right SHIFT key is locked.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_LWINLATCHED"></a><a id="skf_lwinlatched"></a><dl>
<dt><b>SKF_LWINLATCHED</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The left Windows key is latched.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_RWINLATCHED"></a><a id="skf_rwinlatched"></a><dl>
<dt><b>SKF_RWINLATCHED</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The right Windows key is latched.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_LWINLOCKED"></a><a id="skf_lwinlocked"></a><dl>
<dt><b>SKF_LWINLOCKED</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The left Windows key is locked.

</td>
</tr>
<tr>
<td width="40%"><a id="SKF_RWINLOCKED"></a><a id="skf_rwinlocked"></a><dl>
<dt><b>SKF_RWINLOCKED</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
<b>Windows 98, Windows 2000: </b> The right Windows key is locked.

</td>
</tr>
</table>

## -remarks

An application uses a <b>STICKYKEYS</b> structure when calling the <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function with the <i>uiAction</i> parameter set to <b>SPI_GETSTICKYKEYS</b> or <b>SPI_SETSTICKYKEYS</b>. When using <b>SPI_GETSTICKYKEYS</b>, you must specify the <b>cbSize</b> member of the <b>STICKYKEYS</b> structure; the <b>SystemParametersInfo</b> function fills the remaining members. You must specify all structure members when using the <b>SPI_SETSTICKYKEYS</b> value.

If you call <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> with the <b>SPI_SETSTICKYKEYS</b> value, the following flags are ignored:

<ul>
<li>SKF_LALTLATCHED</li>
<li>SKF_LCTLLATCHED</li>
<li>SKF_LSHIFTLATCHED</li>
<li>SKF_RALTLATCHED</li>
<li>SKF_RCTLLATCHED</li>
<li>SKF_RSHIFTLATCHED</li>
<li>SKF_LALTLOCKED</li>
<li>SKF_LCTLLOCKED</li>
<li>SKF_LSHIFTLOCKED</li>
<li>SKF_RALTLOCKED</li>
<li>SKF_RCTLLOCKED</li>
<li>SKF_RSHIFTLOCKED</li>
</ul>

## -see-also

<a href="/windows/desktop/WinAuto/accessibility-structures">Accessibility Structures</a>



<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>