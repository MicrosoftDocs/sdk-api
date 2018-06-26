---
UID: NS:winuser.tagMSLLHOOKSTRUCT
title: tagMSLLHOOKSTRUCT
author: windows-sdk-content
description: Contains information about a low-level mouse input event.
old-location: winmsg\msllhookstruct.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\msllhookstruct.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: "*LPMSLLHOOKSTRUCT, *PMSLLHOOKSTRUCT, LLMHF_INJECTED, LLMHF_LOWER_IL_INJECTED, LPMSLLHOOKSTRUCT, LPMSLLHOOKSTRUCT structure pointer [Windows and Messages], MSLLHOOKSTRUCT, MSLLHOOKSTRUCT structure [Windows and Messages], PMSLLHOOKSTRUCT, PMSLLHOOKSTRUCT structure pointer [Windows and Messages], XBUTTON1, XBUTTON2, _win32_MSLLHOOKSTRUCT_str, _win32_msllhookstruct_str_cpp, tagMSLLHOOKSTRUCT, winmsg.msllhookstruct, winui._win32_msllhookstruct_str, winuser/LPMSLLHOOKSTRUCT, winuser/MSLLHOOKSTRUCT, winuser/PMSLLHOOKSTRUCT"
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
req.typenames: MSLLHOOKSTRUCT, *LPMSLLHOOKSTRUCT, *PMSLLHOOKSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - MSLLHOOKSTRUCT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagMSLLHOOKSTRUCT structure


## -description


Contains information about a low-level mouse input event. 


## -struct-fields




### -field pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

The x- and y-coordinates of the cursor, in <a href="https://msdn.microsoft.com/library/windows/desktop/dn280512(v=vs.85).aspx(d=robot)">per-monitor-aware</a> screen coordinates. 


### -field mouseData

Type: <b>DWORD</b>

If the message is <a href="https://msdn.microsoft.com/9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb">WM_MOUSEWHEEL</a>, the high-order word of this member is the wheel delta. The low-order word is reserved. A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user. One wheel click is defined as <b>WHEEL_DELTA</b>, which is 120.

If the message is <a href="https://msdn.microsoft.com/4d972841-1513-4925-9d59-2557233561a2">WM_XBUTTONDOWN</a>, <a href="https://msdn.microsoft.com/ad726859-368a-4603-bffa-4e639bc69a6a">WM_XBUTTONUP</a>, <a href="https://msdn.microsoft.com/68f7abaf-cf6d-499a-957f-3c4d73cdbdee">WM_XBUTTONDBLCLK</a>, <a href="https://msdn.microsoft.com/72744c98-1898-4548-bd10-61ad53eeab15">WM_NCXBUTTONDOWN</a>, <a href="https://msdn.microsoft.com/07ab5d4e-9912-4867-9146-8abc5addc15d">WM_NCXBUTTONUP</a>, or <a href="https://msdn.microsoft.com/8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef">WM_NCXBUTTONDBLCLK</a>, the high-order word specifies which X button was pressed or released, and the low-order word is reserved. This value can be one or more of the following values. Otherwise, 
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



<a href="https://msdn.microsoft.com/987095d7-059f-4eae-925d-6723ab6d524c">Hooks</a>



<a href="https://msdn.microsoft.com/a0922155-22e5-410a-b64e-f87690de8a17">LowLevelMouseProc</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/66c96282-528c-4f57-acab-ae03178e4fe9">SetWindowsHookEx</a>



<a href="https://msdn.microsoft.com/9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb">WM_MOUSEWHEEL</a>



<a href="https://msdn.microsoft.com/8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef">WM_NCXBUTTONDBLCLK</a>



<a href="https://msdn.microsoft.com/72744c98-1898-4548-bd10-61ad53eeab15">WM_NCXBUTTONDOWN</a>



<a href="https://msdn.microsoft.com/07ab5d4e-9912-4867-9146-8abc5addc15d">WM_NCXBUTTONUP</a>



<a href="https://msdn.microsoft.com/68f7abaf-cf6d-499a-957f-3c4d73cdbdee">WM_XBUTTONDBLCLK</a>



<a href="https://msdn.microsoft.com/4d972841-1513-4925-9d59-2557233561a2">WM_XBUTTONDOWN</a>



<a href="https://msdn.microsoft.com/ad726859-368a-4603-bffa-4e639bc69a6a">WM_XBUTTONUP</a>
 

 

