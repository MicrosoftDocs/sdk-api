---
UID: NS:winuser.tagRAWKEYBOARD
title: tagRAWKEYBOARD
author: windows-sdk-content
description: Contains information about the state of the keyboard.
old-location: inputdev\rawkeyboard.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawkeyboard.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPRAWKEYBOARD, *PRAWKEYBOARD, LPRAWKEYBOARD, LPRAWKEYBOARD structure pointer [Keyboard and Mouse Input], PRAWKEYBOARD, PRAWKEYBOARD structure pointer [Keyboard and Mouse Input], RAWKEYBOARD, RAWKEYBOARD structure [Keyboard and Mouse Input], RI_KEY_BREAK, RI_KEY_E0, RI_KEY_E1, RI_KEY_MAKE, _win32_RAWKEYBOARD_str, _win32_rawkeyboard_str_cpp, inputdev.rawkeyboard, tagRAWKEYBOARD, winui._win32_rawkeyboard_str, winuser/LPRAWKEYBOARD, winuser/PRAWKEYBOARD, winuser/RAWKEYBOARD"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: RAWKEYBOARD, *PRAWKEYBOARD, *LPRAWKEYBOARD
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

Windows message compatible virtual-key code. For more information, see <a href="https://msdn.microsoft.com/fa8926ad-41b2-4164-9ba3-ae501fd0eef2">Virtual Key Codes</a>. 


### -field Message

Type: <b>UINT</b>

The corresponding window message, for example <a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a>, <a href="https://msdn.microsoft.com/a3c03dbf-1be7-49ff-b931-1981786b74ce">WM_SYSKEYDOWN</a>, and so forth. 


### -field ExtraInformation

Type: <b>ULONG</b>

The device-specific additional information for the event. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1d8316d3-83ed-4f8b-bed4-09533d6f3591">GetRawInputDeviceInfo</a>



<a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a>



<a href="https://msdn.microsoft.com/a2afdb80-d68a-4c33-826f-96739d239cd9">Raw Input</a>



<b>Reference</b>
 

 

