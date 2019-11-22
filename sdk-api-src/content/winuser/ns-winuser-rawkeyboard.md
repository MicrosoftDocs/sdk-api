---
UID: NS:winuser.tagRAWKEYBOARD
title: RAWKEYBOARD (winuser.h)

description: Contains information about the state of the keyboard.
old-location: inputdev\rawkeyboard.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawkeyboard.htm

ms.date: 12/05/2018
ms.keywords: "*LPRAWKEYBOARD, *PRAWKEYBOARD, LPRAWKEYBOARD, LPRAWKEYBOARD structure pointer [Keyboard and Mouse Input], PRAWKEYBOARD, PRAWKEYBOARD structure pointer [Keyboard and Mouse Input], RAWKEYBOARD, RAWKEYBOARD structure [Keyboard and Mouse Input], RI_KEY_BREAK, RI_KEY_E0, RI_KEY_E1, RI_KEY_MAKE, _win32_RAWKEYBOARD_str, _win32_rawkeyboard_str_cpp, inputdev.rawkeyboard, winui._win32_rawkeyboard_str, winuser/LPRAWKEYBOARD, winuser/PRAWKEYBOARD, winuser/RAWKEYBOARD"
ms.topic: struct
f1_keywords: 
 - "winuser/RAWKEYBOARD"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: RAWKEYBOARD, *PRAWKEYBOARD, *LPRAWKEYBOARD
req.redist: 
ms.custom: 19H1
---

# RAWKEYBOARD structure


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

Windows message compatible virtual-key code. For more information, see <a href="https://docs.microsoft.com/windows/desktop/inputdev/virtual-key-codes">Virtual Key Codes</a>. 


### -field Message

Type: <b>UINT</b>

The corresponding window message, for example <a href="https://docs.microsoft.com/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>, <a href="https://docs.microsoft.com/windows/desktop/inputdev/wm-syskeydown">WM_SYSKEYDOWN</a>, and so forth. 


### -field ExtraInformation

Type: <b>ULONG</b>

The device-specific additional information for the event. 


## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getrawinputdeviceinfoa">GetRawInputDeviceInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-rawinput">RAWINPUT</a>



<a href="https://docs.microsoft.com/windows/desktop/inputdev/raw-input">Raw Input</a>



<b>Reference</b>
 

 

