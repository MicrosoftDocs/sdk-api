---
UID: NS:winuser.tagMSLLHOOKSTRUCT
title: MSLLHOOKSTRUCT (winuser.h)
description: Contains information about a low-level mouse input event.
helpviewer_keywords: ["*LPMSLLHOOKSTRUCT","*PMSLLHOOKSTRUCT","LLMHF_INJECTED","LLMHF_LOWER_IL_INJECTED","LPMSLLHOOKSTRUCT","LPMSLLHOOKSTRUCT structure pointer [Windows and Messages]","MSLLHOOKSTRUCT","MSLLHOOKSTRUCT structure [Windows and Messages]","PMSLLHOOKSTRUCT","PMSLLHOOKSTRUCT structure pointer [Windows and Messages]","XBUTTON1","XBUTTON2","_win32_MSLLHOOKSTRUCT_str","_win32_msllhookstruct_str_cpp","winmsg.msllhookstruct","winui._win32_msllhookstruct_str","winuser/LPMSLLHOOKSTRUCT","winuser/MSLLHOOKSTRUCT","winuser/PMSLLHOOKSTRUCT"]
old-location: winmsg\msllhookstruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\msllhookstruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPMSLLHOOKSTRUCT, *PMSLLHOOKSTRUCT, LLMHF_INJECTED, LLMHF_LOWER_IL_INJECTED, LPMSLLHOOKSTRUCT, LPMSLLHOOKSTRUCT structure pointer [Windows and Messages], MSLLHOOKSTRUCT, MSLLHOOKSTRUCT structure [Windows and Messages], PMSLLHOOKSTRUCT, PMSLLHOOKSTRUCT structure pointer [Windows and Messages], XBUTTON1, XBUTTON2, _win32_MSLLHOOKSTRUCT_str, _win32_msllhookstruct_str_cpp, winmsg.msllhookstruct, winui._win32_msllhookstruct_str, winuser/LPMSLLHOOKSTRUCT, winuser/MSLLHOOKSTRUCT, winuser/PMSLLHOOKSTRUCT'
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
req.typenames: MSLLHOOKSTRUCT, *LPMSLLHOOKSTRUCT, *PMSLLHOOKSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMSLLHOOKSTRUCT
 - winuser/tagMSLLHOOKSTRUCT
 - LPMSLLHOOKSTRUCT
 - winuser/LPMSLLHOOKSTRUCT
 - MSLLHOOKSTRUCT
 - winuser/MSLLHOOKSTRUCT
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
 - MSLLHOOKSTRUCT
---

# MSLLHOOKSTRUCT structure


## -description

Contains information about a low-level mouse input event.

## -struct-fields

### -field pt

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The x- and y-coordinates of the cursor, in <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness">per-monitor-aware</a> screen coordinates.

### -field mouseData

Type: <b>DWORD</b>

If the message is <a href="/windows/desktop/inputdev/wm-mousewheel">WM_MOUSEWHEEL</a>, the high-order word of this member is the wheel delta. The low-order word is reserved. A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user. One wheel click is defined as <b>WHEEL_DELTA</b>, which is 120.

If the message is <a href="/windows/desktop/inputdev/wm-xbuttondown">WM_XBUTTONDOWN</a>, <a href="/windows/desktop/inputdev/wm-xbuttonup">WM_XBUTTONUP</a>, <a href="/windows/desktop/inputdev/wm-xbuttondblclk">WM_XBUTTONDBLCLK</a>, <a href="/windows/desktop/inputdev/wm-ncxbuttondown">WM_NCXBUTTONDOWN</a>, <a href="/windows/desktop/inputdev/wm-ncxbuttonup">WM_NCXBUTTONUP</a>, or <a href="/windows/desktop/inputdev/wm-ncxbuttondblclk">WM_NCXBUTTONDBLCLK</a>, the high-order word specifies which X button was pressed or released, and the low-order word is reserved. This value can be one or more of the following values. Otherwise, 
						<b>mouseData</b> is not used. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XBUTTON1"></a><a id="xbutton1"></a><dl>
<dt><b>XBUTTON1</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The first X button was pressed or released.

</td>
</tr>
<tr>
<td width="40%"><a id="XBUTTON2"></a><a id="xbutton2"></a><dl>
<dt><b>XBUTTON2</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The second X button was pressed or released.

</td>
</tr>
</table>

### -field flags

Type: <b>DWORD</b>

The event-injected flags. An application can use the following values to test the flags. Testing LLMHF_INJECTED (bit 0) will tell you whether the event was injected. If it was, then testing LLMHF_LOWER_IL_INJECTED (bit 1) will tell you whether or not the event was injected from a process running at lower integrity level.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LLMHF_INJECTED"></a><a id="llmhf_injected"></a><dl>
<dt><b>LLMHF_INJECTED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Test the event-injected (from any process) flag.

</td>
</tr>
<tr>
<td width="40%"><a id="LLMHF_LOWER_IL_INJECTED"></a><a id="llmhf_lower_il_injected"></a><dl>
<dt><b>LLMHF_LOWER_IL_INJECTED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Test the event-injected (from a process running at lower integrity level) flag.

</td>
</tr>
</table>

### -field time

Type: <b>DWORD</b>

The time stamp for this message.

### -field dwExtraInfo

Type: <b>ULONG_PTR</b>

Additional information associated with the message.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/winmsg/hooks">Hooks</a>



<a href="/windows/win32/winmsg/lowlevelmouseproc">LowLevelMouseProc</a>



<b>Other Resources</b>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>



<a href="/windows/desktop/inputdev/wm-mousewheel">WM_MOUSEWHEEL</a>



<a href="/windows/desktop/inputdev/wm-ncxbuttondblclk">WM_NCXBUTTONDBLCLK</a>



<a href="/windows/desktop/inputdev/wm-ncxbuttondown">WM_NCXBUTTONDOWN</a>



<a href="/windows/desktop/inputdev/wm-ncxbuttonup">WM_NCXBUTTONUP</a>



<a href="/windows/desktop/inputdev/wm-xbuttondblclk">WM_XBUTTONDBLCLK</a>



<a href="/windows/desktop/inputdev/wm-xbuttondown">WM_XBUTTONDOWN</a>



<a href="/windows/desktop/inputdev/wm-xbuttonup">WM_XBUTTONUP</a>