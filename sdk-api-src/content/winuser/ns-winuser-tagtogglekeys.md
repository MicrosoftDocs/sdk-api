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

# tagTOGGLEKEYS structure


## -description



        Contains information about the ToggleKeys accessibility feature. When the ToggleKeys feature is on, the computer emits a high-pitched tone whenever the user turns on the CAPS LOCK, NUM LOCK, or SCROLL LOCK key, and a low-pitched tone whenever the user turns off one of those keys.
      


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the size, in bytes, of this structure.


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


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



An application uses a <b>TOGGLEKEYS</b> structure when calling the <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a> function with the <i>uiAction</i> parameter set to <b>SPI_GETTOGGLEKEYS</b> or <b>SPI_SETTOGGLEKEYS</b>. When using SPI_GETTOGGLEKEYS, an application must specify the <b>cbSize</b> member of the <b>TOGGLEKEYS</b> structure; the <b>SystemParametersInfo</b> function fills the remaining members. An application must specify all structure members when using the <b>SPI_SETTOGGLEKEYS</b> value.




## -see-also




<a href="https://msdn.microsoft.com/0ff480ae-18e3-413d-b208-a67fbae28c25">Accessibility Structures</a>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>
 

 

