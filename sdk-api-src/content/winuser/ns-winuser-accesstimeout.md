---
UID: NS:winuser.tagACCESSTIMEOUT
title: ACCESSTIMEOUT (winuser.h)
description: Contains information about the time-out period associated with the accessibility features.
helpviewer_keywords: ["*LPACCESSTIMEOUT","ACCESSTIMEOUT","ACCESSTIMEOUT structure [Windows Accessibility]","ATF_ONOFFFEEDBACK","ATF_TIMEOUTON","LPACCESSTIMEOUT","LPACCESSTIMEOUT structure pointer [Windows Accessibility]","_win32_ACCESSTIMEOUT_str","msaa.accesstimeout","tagACCESSTIMEOUT","winauto.accesstimeout","winuser/ACCESSTIMEOUT","winuser/LPACCESSTIMEOUT"]
old-location: winauto\accesstimeout.htm
tech.root: WinAuto
ms.assetid: 570a3a29-a7ce-4622-affd-7c6c4f381e36
ms.date: 12/05/2018
ms.keywords: '*LPACCESSTIMEOUT, ACCESSTIMEOUT, ACCESSTIMEOUT structure [Windows Accessibility], ATF_ONOFFFEEDBACK, ATF_TIMEOUTON, LPACCESSTIMEOUT, LPACCESSTIMEOUT structure pointer [Windows Accessibility], _win32_ACCESSTIMEOUT_str, msaa.accesstimeout, tagACCESSTIMEOUT, winauto.accesstimeout, winuser/ACCESSTIMEOUT, winuser/LPACCESSTIMEOUT'
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
req.typenames: ACCESSTIMEOUT, *LPACCESSTIMEOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagACCESSTIMEOUT
 - winuser/tagACCESSTIMEOUT
 - LPACCESSTIMEOUT
 - winuser/LPACCESSTIMEOUT
 - ACCESSTIMEOUT
 - winuser/ACCESSTIMEOUT
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
 - ACCESSTIMEOUT
---

# ACCESSTIMEOUT structure


## -description

Contains information about the time-out period associated with the Microsoft Win32 accessibility features. 

The accessibility time-out period is the length of time that must pass without keyboard and mouse input before the operating system automatically turns off accessibility features. The accessibility time-out is designed for computers that are shared by several users so that options selected by one user do not inconvenience a subsequent user.

The accessibility features affected by the time-out are
        the FilterKeys features (SlowKeys, BounceKeys, and
        RepeatKeys), MouseKeys, ToggleKeys, and StickyKeys. The
        accessibility time-out also affects the high contrast mode
        setting.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the size, in bytes, of this structure.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A set of bit flags that specify properties of the time-out behavior for accessibility features. The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ATF_ONOFFFEEDBACK"></a><a id="atf_onofffeedback"></a><dl>
<dt><b>ATF_ONOFFFEEDBACK</b></dt>
<dt>0x00000002
</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the operating system plays a descending siren sound when the time-out period elapses and the accessibility features are turned off.

</td>
</tr>
<tr>
<td width="40%"><a id="ATF_TIMEOUTON"></a><a id="atf_timeouton"></a><dl>
<dt><b>ATF_TIMEOUTON</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this flag is set, a time-out period has been set for accessibility features. If this flag is not set, the features will not time out even though a time-out period is specified.

</td>
</tr>
</table>

### -field iTimeOutMSec

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the time-out period, in milliseconds.

## -remarks

Use an <b>ACCESSTIMEOUT</b> structure when calling the <a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function with the <i>uiAction</i> parameter set to the <b>SPI_GETACCESSTIMEOUT</b> or <b>SPI_SETACCESSTIMEOUT</b> value. When using <b>SPI_GETACCESSTIMEOUT</b>, you must specify the <b>cbSize</b> member of the <b>ACCESSTIMEOUT</b> structure; the <b>SystemParametersInfo</b> function fills in the remaining members. Specify all structure members when using the <b>SPI_SETACCESSTIMEOUT</b> value.

## -see-also

<a href="/windows/desktop/WinAuto/accessibility-structures">Accessibility Structures</a>



<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>