---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagACCESSTIMEOUT structure


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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the size, in bytes, of this structure.


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the time-out period, in milliseconds.


## -remarks



Use an <b>ACCESSTIMEOUT</b> structure when calling the <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function with the <i>uiAction</i> parameter set to the <b>SPI_GETACCESSTIMEOUT</b> or <b>SPI_SETACCESSTIMEOUT</b> value. When using <b>SPI_GETACCESSTIMEOUT</b>, you must specify the <b>cbSize</b> member of the <b>ACCESSTIMEOUT</b> structure; the <b>SystemParametersInfo</b> function fills in the remaining members. Specify all structure members when using the <b>SPI_SETACCESSTIMEOUT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/0ff480ae-18e3-413d-b208-a67fbae28c25">Accessibility Structures</a>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>
 

 

