---
UID: NF:winuser.GetScrollRange
title: GetScrollRange function
author: windows-sdk-content
description: The GetScrollRange function retrieves the current minimum and maximum scroll box (thumb) positions for the specified scroll bar.
old-location: controls\GetScrollRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\getscrollrange.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetScrollRange, GetScrollRange function [Windows Controls], SB_CTL, SB_HORZ, SB_VERT, _win32_GetScrollRange, _win32_GetScrollRange_cpp, controls.GetScrollRange, controls._win32_GetScrollRange, winuser/GetScrollRange
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetScrollRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetScrollRange function


## -description


The <b>GetScrollRange</b> function retrieves the current minimum and maximum scroll box (thumb) positions for the specified scroll bar.

			
<div class="alert"><b>Note</b>  The <b>GetScrollRange</b> function is provided for compatibility only. New applications should use the <a href="https://msdn.microsoft.com/c4bd075b-b4fd-44cf-ba51-b9d8a95a5152">GetScrollInfo</a> function.</div><div> </div>

## -parameters




### -param hWnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a scroll bar control or a window with a standard scroll bar, depending on the value of the 
					<i>nBar</i> parameter. 


### -param nBar [in]

Type: <b>int</b>

Specifies the scroll bar from which the positions are retrieved. This parameter can be one of the following values. 

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
Retrieves the positions of a scroll bar control. The 
						<i>hWnd</i> parameter must be the handle to the scroll bar control.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the positions of the window's standard horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the positions of the window's standard vertical scroll bar.

</td>
</tr>
</table>
 


### -param lpMinPos [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPINT</a></b>

Pointer to the integer variable that receives the minimum position. 


### -param lpMaxPos [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPINT</a></b>

Pointer to the integer variable that receives the maximum position. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If the specified window does not have standard scroll bars or is not a scroll bar control, the <b>GetScrollRange</b> function copies zero to the 
				<i>lpMinPos</i> and 
				<i>lpMaxPos</i> parameters. 

The default range for a standard scroll bar is 0 through 100. The default range for a scroll bar control is empty (both values are zero). 

The messages that indicate scroll bar position, <a href="https://msdn.microsoft.com/197e522f-defd-4356-8521-5b5dfda596da">WM_HSCROLL</a> and <a href="https://msdn.microsoft.com/495733b8-1aac-4ff7-b0be-15f14581f41c">WM_VSCROLL</a>, are limited to 16 bits of position data. However, because <a href="https://msdn.microsoft.com/a45af17c-df18-4156-be8b-868fc4cb0696">SetScrollInfo</a>, <a href="https://msdn.microsoft.com/068d874d-ea9e-4953-93b3-9e90141d4e50">SetScrollPos</a>, <a href="https://msdn.microsoft.com/749c3b04-d5a6-4f7c-89a3-a1c0fbb85cb9">SetScrollRange</a>, <a href="https://msdn.microsoft.com/c4bd075b-b4fd-44cf-ba51-b9d8a95a5152">GetScrollInfo</a>, <a href="https://msdn.microsoft.com/8d8c43df-c444-4c0a-82e5-bdc568161561">GetScrollPos</a>, and <b>GetScrollRange</b> support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the <b>WM_HSCROLL</b> and <b>WM_VSCROLL</b> messages. See the <b>GetScrollInfo</b> function for a description of the technique. 

If the <i>nBar</i> parameter is SB_CTL and the window specified by the <i>hWnd</i> parameter is not a system scroll bar control, the system sends the <a href="https://msdn.microsoft.com/661a9491-3bf6-4685-aea0-c5e4126313af">SBM_GETRANGE</a> message to the window to obtain scroll bar information.  This allows <b>GetScrollRange</b> to operate on a custom control that mimics a scroll bar.  If the window does not handle the <b>SBM_GETRANGE</b> message, the <b>GetScrollRange</b> function fails.




## -see-also




<a href="https://msdn.microsoft.com/c4bd075b-b4fd-44cf-ba51-b9d8a95a5152">GetScrollInfo</a>



<a href="https://msdn.microsoft.com/8d8c43df-c444-4c0a-82e5-bdc568161561">GetScrollPos</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a45af17c-df18-4156-be8b-868fc4cb0696">SetScrollInfo</a>



<a href="https://msdn.microsoft.com/068d874d-ea9e-4953-93b3-9e90141d4e50">SetScrollPos</a>



<a href="https://msdn.microsoft.com/749c3b04-d5a6-4f7c-89a3-a1c0fbb85cb9">SetScrollRange</a>



<a href="https://msdn.microsoft.com/197e522f-defd-4356-8521-5b5dfda596da">WM_HSCROLL</a>



<a href="https://msdn.microsoft.com/495733b8-1aac-4ff7-b0be-15f14581f41c">WM_VSCROLL</a>
 

 

