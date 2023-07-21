---
UID: NS:winuser.tagKBDLLHOOKSTRUCT
title: KBDLLHOOKSTRUCT (winuser.h)
description: Contains information about a low-level keyboard input event.
helpviewer_keywords: ["*LPKBDLLHOOKSTRUCT","*PKBDLLHOOKSTRUCT","KBDLLHOOKSTRUCT","KBDLLHOOKSTRUCT structure [Windows and Messages]","LLKHF_ALTDOWN","LLKHF_EXTENDED","LLKHF_INJECTED","LLKHF_LOWER_IL_INJECTED","LLKHF_UP","LPKBDLLHOOKSTRUCT","LPKBDLLHOOKSTRUCT structure pointer [Windows and Messages]","PKBDLLHOOKSTRUCT","PKBDLLHOOKSTRUCT structure pointer [Windows and Messages]","_win32_KBDLLHOOKSTRUCT_str","_win32_kbdllhookstruct_str_cpp","winmsg.kbdllhookstruct","winui._win32_kbdllhookstruct_str","winuser/KBDLLHOOKSTRUCT","winuser/LPKBDLLHOOKSTRUCT","winuser/PKBDLLHOOKSTRUCT"]
old-location: winmsg\kbdllhookstruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\kbdllhookstruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPKBDLLHOOKSTRUCT, *PKBDLLHOOKSTRUCT, KBDLLHOOKSTRUCT, KBDLLHOOKSTRUCT structure [Windows and Messages], LLKHF_ALTDOWN, LLKHF_EXTENDED, LLKHF_INJECTED, LLKHF_LOWER_IL_INJECTED, LLKHF_UP, LPKBDLLHOOKSTRUCT, LPKBDLLHOOKSTRUCT structure pointer [Windows and Messages], PKBDLLHOOKSTRUCT, PKBDLLHOOKSTRUCT structure pointer [Windows and Messages], _win32_KBDLLHOOKSTRUCT_str, _win32_kbdllhookstruct_str_cpp, winmsg.kbdllhookstruct, winui._win32_kbdllhookstruct_str, winuser/KBDLLHOOKSTRUCT, winuser/LPKBDLLHOOKSTRUCT, winuser/PKBDLLHOOKSTRUCT'
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
req.typenames: KBDLLHOOKSTRUCT, *LPKBDLLHOOKSTRUCT, *PKBDLLHOOKSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagKBDLLHOOKSTRUCT
 - winuser/tagKBDLLHOOKSTRUCT
 - LPKBDLLHOOKSTRUCT
 - winuser/LPKBDLLHOOKSTRUCT
 - KBDLLHOOKSTRUCT
 - winuser/KBDLLHOOKSTRUCT
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
 - KBDLLHOOKSTRUCT
---

# KBDLLHOOKSTRUCT structure


## -description

Contains information about a low-level keyboard input event.

## -struct-fields

### -field vkCode

Type: <b>DWORD</b>

A <a href="/windows/desktop/inputdev/virtual-key-codes">virtual-key code</a>. The code must be a value in the range 1 to 254.

### -field scanCode

Type: <b>DWORD</b>

A hardware scan code for the key.

### -field flags

Type: <b>DWORD</b>

The extended-key flag, event-injected flags, context code, and transition-state flag. This member is specified as follows. An application can use the following values to test the keystroke flags. Testing LLKHF_INJECTED (bit 4) will tell you whether the event was injected. If it was, then testing LLKHF_LOWER_IL_INJECTED (bit 1) will tell you whether or not the event was injected from a process running at lower integrity level.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LLKHF_EXTENDED"></a><a id="llkhf_extended"></a><dl>
<dt><b>LLKHF_EXTENDED</b></dt>
<dt>(KF_EXTENDED &gt;&gt; 8)</dt>
</dl>
</td>
<td width="60%">
Test the extended-key flag. 

</td>
</tr>
<tr>
<td width="40%"><a id="LLKHF_LOWER_IL_INJECTED"></a><a id="llkhf_lower_il_injected"></a><dl>
<dt><b>LLKHF_LOWER_IL_INJECTED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Test the event-injected (from a process running at lower integrity level) flag.

</td>
</tr>
<tr>
<td width="40%"><a id="LLKHF_INJECTED"></a><a id="llkhf_injected"></a><dl>
<dt><b>LLKHF_INJECTED</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Test the event-injected (from any process) flag.

</td>
</tr>
<tr>
<td width="40%"><a id="LLKHF_ALTDOWN"></a><a id="llkhf_altdown"></a><dl>
<dt><b>LLKHF_ALTDOWN</b></dt>
<dt>(KF_ALTDOWN &gt;&gt; 8)</dt>
</dl>
</td>
<td width="60%">
Test the context code. 

</td>
</tr>
<tr>
<td width="40%"><a id="LLKHF_UP"></a><a id="llkhf_up"></a><dl>
<dt><b>LLKHF_UP</b></dt>
<dt>(KF_UP &gt;&gt; 8)</dt>
</dl>
</td>
<td width="60%">
Test the transition-state flag. 

</td>
</tr>
</table>
 

The following table describes the layout of this value.

<table>
<tr>
<th>Bits</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Specifies whether the key is an extended key, such as a function key or a key on the numeric keypad. The value is 1 if the key is an extended key; otherwise, it is 0.</td>
</tr>
<tr>
<td>1</td>
<td>Specifies whether the event was injected from a process running at lower integrity level. The value is 1 if that is the case; otherwise, it is 0. Note that bit 4 is also set whenever bit 1 is set.</td>
</tr>
<tr>
<td>2-3</td>
<td>Reserved.</td>
</tr>
<tr>
<td>4</td>
<td>Specifies whether the event was injected. The value is 1 if that is the case; otherwise, it is 0. Note that bit 1 is not necessarily set when bit 4 is set.</td>
</tr>
<tr>
<td>5</td>
<td>The context code. The value is 1 if the ALT key is pressed; otherwise, it is 0.</td>
</tr>
<tr>
<td>6</td>
<td>Reserved.</td>
</tr>
<tr>
<td>7</td>
<td>The transition state. The value is 0 if the key is pressed and 1 if it is being released.</td>
</tr>
</table>

### -field time

Type: <b>DWORD</b>

The time stamp for this message, equivalent to what <a href="/windows/desktop/api/winuser/nf-winuser-getmessagetime">GetMessageTime</a> would return for this message.

### -field dwExtraInfo

Type: <b>ULONG_PTR</b>

Additional information associated with the message.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/winmsg/hooks">Hooks</a>

[LowLevelKeyboardProc](/windows/win32/winmsg/lowlevelkeyboardproc)


<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>