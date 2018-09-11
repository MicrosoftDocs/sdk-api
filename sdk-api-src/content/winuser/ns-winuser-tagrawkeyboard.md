---
UID: NS:winuser.tagRAWKEYBOARD
title: tagRAWKEYBOARD
author: windows-sdk-content
description: Contains information about the state of the keyboard.
old-location: inputdev\rawkeyboard.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawkeyboard.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: "*LPRAWKEYBOARD, *PRAWKEYBOARD, LPRAWKEYBOARD, LPRAWKEYBOARD structure pointer [Keyboard and Mouse Input], PRAWKEYBOARD, PRAWKEYBOARD structure pointer [Keyboard and Mouse Input], RAWKEYBOARD, RAWKEYBOARD structure [Keyboard and Mouse Input], RI_KEY_BREAK, RI_KEY_E0, RI_KEY_E1, RI_KEY_MAKE, _win32_RAWKEYBOARD_str, _win32_rawkeyboard_str_cpp, inputdev.rawkeyboard, tagRAWKEYBOARD, winui._win32_rawkeyboard_str, winuser/LPRAWKEYBOARD, winuser/PRAWKEYBOARD, winuser/RAWKEYBOARD"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - RAWKEYBOARD
product: Windows
targetos: Windows
req.typenames: RAWKEYBOARD, *PRAWKEYBOARD, *LPRAWKEYBOARD
req.redist: 
---

# tagRAWKEYBOARD structure


## -description


Contains information about the state of the keyboard. 


## -struct-fields




### -field MakeCode

Type: <b>USHORT</b>

The scan code from the key depression. The scan code for keyboard overrun is <b>KEYBOARD_OVERRUN_MAKE_CODE</b>. 


### -field Flags

Type: <b>USHORT</b>

Flags for scan code information. It can be one or more of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RI_KEY_BREAK"></a><a id="ri_key_break"></a><dl>
<dt><b>RI_KEY_BREAK</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The key is up.

</td>
</tr>
<tr>
<td width="40%"><a id="RI_KEY_E0"></a><a id="ri_key_e0"></a><dl>
<dt><b>RI_KEY_E0</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The scan code has the E0 prefix.


</td>
</tr>
<tr>
<td width="40%"><a id="RI_KEY_E1"></a><a id="ri_key_e1"></a><dl>
<dt><b>RI_KEY_E1</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The scan code has the E1 prefix.


</td>
</tr>
<tr>
<td width="40%"><a id="RI_KEY_MAKE"></a><a id="ri_key_make"></a><dl>
<dt><b>RI_KEY_MAKE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The key is down.

</td>
</tr>
</table>
 


### -field Reserved

Type: <b>USHORT</b>

Reserved; must be zero. 


### -field VKey

Type: <b>USHORT</b>

Windows message compatible virtual-key code. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Dd375731(v=VS.85).aspx">Virtual Key Codes</a>. 


### -field Message

Type: <b>UINT</b>

The corresponding window message, for example <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>, <a href="https://msdn.microsoft.com/en-us/library/ms646286(v=VS.85).aspx">WM_SYSKEYDOWN</a>, and so forth. 


### -field ExtraInformation

Type: <b>ULONG</b>

The device-specific additional information for the event. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645597(v=VS.85).aspx">GetRawInputDeviceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645562(v=VS.85).aspx">RAWINPUT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645536(v=VS.85).aspx">Raw Input</a>



<b>Reference</b>
 

 

