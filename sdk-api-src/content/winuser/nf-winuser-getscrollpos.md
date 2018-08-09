---
UID: NF:winuser.GetScrollPos
title: GetScrollPos function
author: windows-sdk-content
description: The GetScrollPos function retrieves the current position of the scroll box (thumb) in the specified scroll bar.
old-location: controls\GetScrollPos.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\getscrollpos.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetScrollPos, GetScrollPos function [Windows Controls], SB_CTL, SB_HORZ, SB_VERT, _win32_GetScrollPos, _win32_GetScrollPos_cpp, controls.GetScrollPos, controls._win32_GetScrollPos, winuser/GetScrollPos
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetScrollPos
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetScrollPos function


## -description


The <b>GetScrollPos</b> function retrieves the current position of the scroll box (thumb) in the specified scroll bar. The current position is a relative value that depends on the current scrolling range. For example, if the scrolling range is 0 through 100 and the scroll box is in the middle of the bar, the current position is 50.

			
<div class="alert"><b>Note</b>   The <b>GetScrollPos</b> function is provided for backward compatibility. New applications should use the <a href="https://msdn.microsoft.com/c4bd075b-b4fd-44cf-ba51-b9d8a95a5152">GetScrollInfo</a> function. </div><div> </div>

## -parameters




### -param hWnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a scroll bar control or a window with a standard scroll bar, depending on the value of the 
					<i>nBar</i> parameter. 


### -param nBar [in]

Type: <b>int</b>

Specifies the scroll bar to be examined. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SB_CTL"></a><a id="sb_ctl"></a><dl>
<dt><b>SB_CTL</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the position of the scroll box in a scroll bar control. The 
						<i>hWnd</i> parameter must be the handle to the scroll bar control.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the position of the scroll box in a window's standard horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the position of the scroll box in a window's standard vertical scroll bar.

</td>
</tr>
</table>
 


## -returns



Type: <b>int</b>

If the function succeeds, the return value is the current position of the scroll box.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>GetScrollPos</b> function enables applications to use 32-bit scroll positions. Although the messages that indicate scroll bar position, <a href="https://msdn.microsoft.com/197e522f-defd-4356-8521-5b5dfda596da">WM_HSCROLL</a> and <a href="https://msdn.microsoft.com/495733b8-1aac-4ff7-b0be-15f14581f41c">WM_VSCROLL</a>, are limited to 16 bits of position data, the functions <a href="https://msdn.microsoft.com/068d874d-ea9e-4953-93b3-9e90141d4e50">SetScrollPos</a>, <a href="https://msdn.microsoft.com/749c3b04-d5a6-4f7c-89a3-a1c0fbb85cb9">SetScrollRange</a>, <b>GetScrollPos</b>, and <a href="https://msdn.microsoft.com/883a7d53-7dc0-4b0c-bcda-e1f022dad12a">GetScrollRange</a> support 32-bit scroll bar position data. Thus, an application can call <b>GetScrollPos</b> while processing either the <b>WM_HSCROLL</b> or <b>WM_VSCROLL</b> messages to obtain 32-bit scroll bar position data. 

To get the 32-bit position of the scroll box (thumb) during a SB_THUMBTRACK request code in a <a href="https://msdn.microsoft.com/197e522f-defd-4356-8521-5b5dfda596da">WM_HSCROLL</a> or <a href="https://msdn.microsoft.com/495733b8-1aac-4ff7-b0be-15f14581f41c">WM_VSCROLL</a> message, use the <a href="https://msdn.microsoft.com/c4bd075b-b4fd-44cf-ba51-b9d8a95a5152">GetScrollInfo</a> function.

If the <i>nBar</i> parameter is SB_CTL and the window specified by the <i>hWnd</i> parameter is not a system scroll bar control, the system sends the <a href="https://msdn.microsoft.com/00344d93-f205-4cda-aa25-6dd065f41b6e">SBM_GETPOS</a> message to the window to obtain scroll bar information.  This allows <b>GetScrollPos</b> to operate on a custom control that mimics a scroll bar.  If the window does not handle the <b>SBM_GETPOS</b> message, the <b>GetScrollPos</b> function fails.




## -see-also




<a href="https://msdn.microsoft.com/c4bd075b-b4fd-44cf-ba51-b9d8a95a5152">GetScrollInfo</a>



<a href="https://msdn.microsoft.com/883a7d53-7dc0-4b0c-bcda-e1f022dad12a">GetScrollRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a45af17c-df18-4156-be8b-868fc4cb0696">SetScrollInfo</a>



<a href="https://msdn.microsoft.com/068d874d-ea9e-4953-93b3-9e90141d4e50">SetScrollPos</a>



<a href="https://msdn.microsoft.com/749c3b04-d5a6-4f7c-89a3-a1c0fbb85cb9">SetScrollRange</a>



<a href="https://msdn.microsoft.com/197e522f-defd-4356-8521-5b5dfda596da">WM_HSCROLL</a>



<a href="https://msdn.microsoft.com/495733b8-1aac-4ff7-b0be-15f14581f41c">WM_VSCROLL</a>
 

 

