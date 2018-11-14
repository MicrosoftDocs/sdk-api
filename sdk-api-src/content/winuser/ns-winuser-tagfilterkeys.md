---
UID: NS:winuser.tagFILTERKEYS
title: tagFILTERKEYS
author: windows-sdk-content
description: Contains information about the FilterKeys accessibility feature, which enables a user with disabilities to set the keyboard repeat rate (RepeatKeys), acceptance delay (SlowKeys), and bounce rate (BounceKeys).
old-location: winauto\filterkeys.htm
tech.root: WinAuto
ms.assetid: 6e2526b3-ddf5-425b-8242-b302a683e0ad
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPFILTERKEYS, FILTERKEYS, FILTERKEYS structure [Windows Accessibility], FKF_AVAILABLE, FKF_CLICKON, FKF_CONFIRMHOTKEY, FKF_FILTERKEYSON, FKF_HOTKEYACTIVE, FKF_HOTKEYSOUND, FKF_INDICATOR, LPFILTERKEYS, LPFILTERKEYS structure pointer [Windows Accessibility], _win32_FILTERKEYS_str, msaa.filterkeys, tagFILTERKEYS, winauto.filterkeys, winuser/FILTERKEYS, winuser/LPFILTERKEYS"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - FILTERKEYS
product: Windows
targetos: Windows
req.typenames: FILTERKEYS, *LPFILTERKEYS
req.redist: 
---

# tagFILTERKEYS structure


## -description


Contains information about the FilterKeys accessibility feature, which enables a user with disabilities to set the keyboard repeat rate (RepeatKeys), acceptance delay (SlowKeys), and bounce rate (BounceKeys).
      


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the structure size, in bytes.


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


A set of bit flags that specify properties of the FilterKeys feature. The following bit-flag values are defined:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FKF_AVAILABLE"></a><a id="fkf_available"></a><dl>
<dt><b>FKF_AVAILABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The FilterKeys features are available.

</td>
</tr>
<tr>
<td width="40%"><a id="FKF_CLICKON"></a><a id="fkf_clickon"></a><dl>
<dt><b>FKF_CLICKON</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The computer makes a click sound when a key is pressed or accepted. If SlowKeys is on, a click is generated when the key is pressed and again when the keystroke is accepted.

</td>
</tr>
<tr>
<td width="40%"><a id="FKF_CONFIRMHOTKEY"></a><a id="fkf_confirmhotkey"></a><dl>
<dt><b>FKF_CONFIRMHOTKEY</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95/98, Windows 2000:</b> A confirmation dialog box appears when the FilterKeys features are activated by using the hot key.

</td>
</tr>
<tr>
<td width="40%"><a id="FKF_FILTERKEYSON"></a><a id="fkf_filterkeyson"></a><dl>
<dt><b>FKF_FILTERKEYSON</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The FilterKeys features are on.

</td>
</tr>
<tr>
<td width="40%"><a id="FKF_HOTKEYACTIVE"></a><a id="fkf_hotkeyactive"></a><dl>
<dt><b>FKF_HOTKEYACTIVE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The user can turn the FilterKeys feature on and off by holding down the RIGHT SHIFT key for eight seconds.

</td>
</tr>
<tr>
<td width="40%"><a id="FKF_HOTKEYSOUND"></a><a id="fkf_hotkeysound"></a><dl>
<dt><b>FKF_HOTKEYSOUND</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the computer plays a siren sound when the user turns the FilterKeys feature on or off by using the hot key.

</td>
</tr>
<tr>
<td width="40%"><a id="FKF_INDICATOR"></a><a id="fkf_indicator"></a><dl>
<dt><b>FKF_INDICATOR</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
<b>Windows 95, Windows 2000:</b> A visual indicator is displayed when the FilterKeys features are on.

</td>
</tr>
</table>
 


### -field iWaitMSec

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the length of time, in milliseconds, that the user must hold down a key before it is accepted by the computer.


### -field iDelayMSec

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the length of time, in milliseconds, that the user must hold down a key before it begins to repeat.


### -field iRepeatMSec

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the length of time, in milliseconds, between each repetition of the keystroke.


### -field iBounceMSec

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the length of time, in milliseconds, that must elapse after releasing a key before the computer will accept a subsequent press of the same key.


## -remarks



Use a <b>FILTERKEYS</b> structure when calling the <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function with the <i>uiAction</i> parameter set to the <b>SPI_GETFILTERKEYS</b> or <b>SPI_SETFILTERKEYS</b> value. When using <b>SPI_GETFILTERKEYS</b>, you must specify the <b>cbSize</b> member of the <b>FILTERKEYS</b> structure; the <b>SystemParametersInfo</b> function fills the remaining members. Specify all structure members when using the <b>SPI_SETFILTERKEYS</b> value.

The <b>iBounceMSec</b> member controls the BounceKeys feature, and the <b>iWaitMSec</b>, <b>iDelayMSec</b>, and <b>iRepeatMSec</b> members work together to control the RepeatKeys and SlowKeys features. If BounceKeys is on (that is, <b>iBounceMSec</b> is nonzero), the RepeatKeys and SlowKeys features are off (that is, the <b>iWaitMSec</b>, <b>iDelayMSec</b>, and <b>iRepeatMSec</b> members must all be zero). Similarly, if BounceKeys is off (<b>iBounceMSec</b> is zero), the <b>iWaitMSec</b>, <b>iDelayMSec</b>, and <b>iRepeatMSec</b> must all be nonzero.

The maximum value of the  <b>iBounceMSec</b>, <b>iWaitMSec</b>, <b>iDelayMSec</b>, and <b>iRepeatMSec</b> members is 20,000 milliseconds.




## -see-also




<a href="https://msdn.microsoft.com/0ff480ae-18e3-413d-b208-a67fbae28c25">Accessibility Structures</a>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>
 

 

