---
UID: NS:winuser.tagHIGHCONTRASTW
title: tagHIGHCONTRASTW
author: windows-sdk-content
description: Contains information about the high contrast accessibility feature.
old-location: winauto\highcontrast.htm
old-project: WinAuto
ms.assetid: 0d8ac624-919a-427a-8374-e256eedc6777
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*LPHIGHCONTRASTW, HCF_AVAILABLE, HCF_CONFIRMHOTKEY, HCF_HIGHCONTRASTON, HCF_HOTKEYACTIVE, HCF_HOTKEYAVAILABLE, HCF_HOTKEYSOUND, HCF_INDICATOR, HIGHCONTRAST, HIGHCONTRAST structure [Windows Accessibility], HIGHCONTRASTW, LPHIGHCONTRAST, LPHIGHCONTRAST structure pointer [Windows Accessibility], _win32_HIGHCONTRAST_str, msaa.highcontrast, tagACCESSTIMEOUTA, tagACCESSTIMEOUTW, tagHIGHCONTRASTW, winauto.highcontrast, winuser/HIGHCONTRAST, winuser/LPHIGHCONTRAST"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: HIGHCONTRASTW, *LPHIGHCONTRASTW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - HIGHCONTRAST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagHIGHCONTRASTW structure


## -description


Contains information about the high contrast accessibility feature.This feature sets the appearance scheme of the user interface for maximum visibility for a visually-impaired user, and advises applications to comply with this appearance scheme.
      


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the size, in bytes, of this structure.


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


Specifies a combination of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
</table>
 


### -field lpszDefaultScheme

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Points to a string that contains the name of the color scheme that will be set to the default scheme.


## -remarks



An application uses this structure when calling the <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function with the <b>SPI_GETHIGHCONTRAST</b> or <b>SPI_SETHIGHCONTRAST</b> value. When using <b>SPI_GETHIGHCONTRAST</b>, an application must specify the <b>cbSize</b> member of the <b>HIGHCONTRAST</b> structure; the <b>SystemParametersInfo</b> function fills the remaining members. An application must specify all structure members when using the <b>SPI_SETHIGHCONTRAST</b> value.




## -see-also




<a href="https://msdn.microsoft.com/0ff480ae-18e3-413d-b208-a67fbae28c25">Accessibility Structures</a>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>
 

 

