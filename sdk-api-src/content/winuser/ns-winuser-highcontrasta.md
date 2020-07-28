---
UID: NS:winuser.tagHIGHCONTRASTA
title: HIGHCONTRASTA (winuser.h)
description: Contains information about the high contrast accessibility feature.
helpviewer_keywords: ["*LPHIGHCONTRASTA","HCF_AVAILABLE","HCF_CONFIRMHOTKEY","HCF_HIGHCONTRASTON","HCF_HOTKEYACTIVE","HCF_HOTKEYAVAILABLE","HCF_HOTKEYSOUND","HCF_INDICATOR","HIGHCONTRAST","HIGHCONTRAST structure [Windows Accessibility]","HIGHCONTRASTA","LPHIGHCONTRAST","LPHIGHCONTRAST structure pointer [Windows Accessibility]","_win32_HIGHCONTRAST_str","msaa.highcontrast","tagACCESSTIMEOUTA","tagACCESSTIMEOUTW","winauto.highcontrast","winuser/HIGHCONTRAST","winuser/LPHIGHCONTRAST"]
old-location: winauto\highcontrast.htm
tech.root: WinAuto
ms.assetid: 0d8ac624-919a-427a-8374-e256eedc6777
ms.date: 12/05/2018
ms.keywords: '*LPHIGHCONTRASTA, HCF_AVAILABLE, HCF_CONFIRMHOTKEY, HCF_HIGHCONTRASTON, HCF_HOTKEYACTIVE, HCF_HOTKEYAVAILABLE, HCF_HOTKEYSOUND, HCF_INDICATOR, HIGHCONTRAST, HIGHCONTRAST structure [Windows Accessibility], HIGHCONTRASTA, LPHIGHCONTRAST, LPHIGHCONTRAST structure pointer [Windows Accessibility], _win32_HIGHCONTRAST_str, msaa.highcontrast, tagACCESSTIMEOUTA, tagACCESSTIMEOUTW, winauto.highcontrast, winuser/HIGHCONTRAST, winuser/LPHIGHCONTRAST'
f1_keywords:
- winuser/HIGHCONTRAST
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Winuser.h
api_name:
- HIGHCONTRAST
targetos: Windows
req.typenames: HIGHCONTRASTA, *LPHIGHCONTRASTA
req.redist: 
ms.custom: 19H1
---

# HIGHCONTRASTA structure

## -description

Contains information about the high contrast accessibility feature.This feature sets the appearance scheme of the user interface for maximum visibility for a visually-impaired user, and advises applications to comply with this appearance scheme.

## -struct-fields

### -field cbSize

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the size, in bytes, of this structure.

### -field dwFlags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies a combination of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HCF_HIGHCONTRASTON"></a><a id="hcf_highcontraston"></a><dl>
<dt><b>HCF_HIGHCONTRASTON</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The high contrast feature is on.
</td>
</tr>
<tr>
<td width="40%"><a id="HCF_AVAILABLE"></a><a id="hcf_available"></a><dl>
<dt><b>HCF_AVAILABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The high contrast feature is available.
</td>
</tr>
<tr>
<td width="40%"><a id="HCF_HOTKEYACTIVE"></a><a id="hcf_hotkeyactive"></a><dl>
<dt><b>HCF_HOTKEYACTIVE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The user can turn the high contrast feature on and off by simultaneously pressing the left ALT, left SHIFT, and PRINT SCREEN keys.
</td>
</tr>
<tr>
<td width="40%"><a id="HCF_CONFIRMHOTKEY"></a><a id="hcf_confirmhotkey"></a><dl>
<dt><b>HCF_CONFIRMHOTKEY</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
A confirmation dialog appears when the high contrast feature is activated by using the hot key.
</td>
</tr>
<tr>
<td width="40%"><a id="HCF_HOTKEYSOUND"></a><a id="hcf_hotkeysound"></a><dl>
<dt><b>HCF_HOTKEYSOUND</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
A siren is played when the user turns the high contrast feature on or off by using the hot key.
</td>
</tr>
<tr>
<td width="40%"><a id="HCF_INDICATOR"></a><a id="hcf_indicator"></a><dl>
<dt><b>HCF_INDICATOR</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
A visual indicator is displayed when the high contrast feature is on. This value is not currently used and is ignored.
</td>
</tr>
<tr>
<td width="40%"><a id="HCF_HOTKEYAVAILABLE"></a><a id="hcf_hotkeyavailable"></a><dl>
<dt><b>HCF_HOTKEYAVAILABLE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The hot key associated with the high contrast feature can be enabled. An application can retrieve this value, but cannot set it.
</td>
</tr>
<tr>
<td width="40%"><a id="HCF_OPTION_NOTHEMECHANGE"></a><a id="hcf_option_nothemechange"></a><dl>
<dt><b>HCF_OPTION_NOTHEMECHANGE</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
<p>Passing HIGHCONTRASTSTRUCTURE in calls to SystemParametersInfoA can cause theme change effects even if the theme isn't being changed. For example, the WM_THEMECHANGED message is sent to Windows even if the only change is to HCF_HOTKEYSOUND.</p>
<p>To prevent this, include the HCF_OPTION_NOTHEMECHANGE flag in the call to SystemParametersInfo.</p>
</td>
> [!NOTE]
> The HCF_OPTION_NOTHEMECHANGE flag should not be used when toggling the high contrast mode (HCF_HIGHCONTRASTON).

</td>
</tr>
<tr>
<td width="40%"><a id="HCF_OPTION_NOFLAGNAME"></a><a id="hcf_option_noflagname"></a><dl>
<dt><b>No flag name supported</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
<p>Passing HIGHCONTRASTSTRUCTURE in calls to the SystemParametersInfoA function can cause theme change effects even if the theme isn't being changed. For example, the WM_THEMECHANGED message is sent to Windows even if the only change is to HCF_HOTKEYSOUND.</p>
<p>To prevent this, include this flag value in the call to SystemParametersInfo.</p>

> [!NOTE]
> This flag should not be used when toggling the high contrast mode (HCF_HIGHCONTRASTON).
</td>
</tr>
</table>

### -field lpszDefaultScheme

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Points to a string that contains the name of the color scheme that will be set to the default scheme.

## -remarks

An application uses this structure when calling the[SystemParametersInfoA function](nf-winuser-systemparametersinfoa.md) with the <b>SPI_GETHIGHCONTRAST</b> or <b>SPI_SETHIGHCONTRAST</b> value. When using <b>SPI_GETHIGHCONTRAST</b>, an application must specify the <b>cbSize</b> member of the <b>HIGHCONTRAST</b> structure; the <b>SystemParametersInfo</b> function fills the remaining members. An application must specify all structure members when using the <b>SPI_SETHIGHCONTRAST</b> value.


> [!NOTE]
> The winuser.h header defines HIGHCONTRAST as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[SystemParametersInfoA function](nf-winuser-systemparametersinfoa.md), [HIGHCONTRASTW structure](ns-winuser-highcontrastw.md), <a href="https://docs.microsoft.com/windows/desktop/WinAuto/accessibility-structures">Accessibility Structures</a>, <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>
