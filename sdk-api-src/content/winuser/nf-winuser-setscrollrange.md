---
UID: NF:winuser.SetScrollRange
title: SetScrollRange function
author: windows-sdk-content
description: The SetScrollRange function sets the minimum and maximum scroll box positions for the specified scroll bar.
old-location: controls\SetScrollRange.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\setscrollrange.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: SB_CTL, SB_HORZ, SB_VERT, SetScrollRange, SetScrollRange function [Windows Controls], _win32_SetScrollRange, _win32_SetScrollRange_cpp, controls.SetScrollRange, controls._win32_SetScrollRange, winuser/SetScrollRange
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
-	Ext-MS-Win-NTUser-Misc-l1-2-0.dll
-	Ext-MS-Win-NTUser-Misc-l1-3-0.dll
-	ext-ms-win-ntuser-misc-l1-3-1.dll
-	Ext-MS-Win-NTUser-Misc-L1-4-0.dll
-	Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
-	Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
-	SetScrollRange
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetScrollRange function


## -description


The <b>SetScrollRange</b> function sets the minimum and maximum scroll box positions for the specified scroll bar. 


<div class="alert"><b>Note</b>  The <b>SetScrollRange</b> function is provided for backward compatibility. New applications should use the <a href="https://msdn.microsoft.com/a45af17c-df18-4156-be8b-868fc4cb0696">SetScrollInfo</a> function.</div><div> </div>

## -parameters




### -param hWnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a scroll bar control or a window with a standard scroll bar, depending on the value of the 
					<i>nBar</i> parameter. 


### -param nBar [in]

Type: <b>int</b>

Specifies the scroll bar to be set. This parameter can be one of the following values. 

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
Sets the range of a scroll bar control. The 
						<i>hwnd</i> parameter must be the handle to the scroll bar control.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Sets the range of a window's standard horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Sets the range of a window's standard vertical scroll bar.

</td>
</tr>
</table>
 


### -param nMinPos [in]

Type: <b>int</b>

Specifies the minimum scrolling position. 


### -param nMaxPos [in]

Type: <b>int</b>

Specifies the maximum scrolling position. 


### -param bRedraw [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether the scroll bar should be redrawn to reflect the change. If this parameter is <b>TRUE</b>, the scroll bar is redrawn. If it is <b>FALSE</b>, the scroll bar is not redrawn. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



You can use <b>SetScrollRange</b> to hide the scroll bar by setting 
				<i>nMinPos</i> and 
				<i>nMaxPos</i> to the same value. An application should not call the <b>SetScrollRange</b> function to hide a scroll bar while processing a scroll bar message. New applications should use the <a href="https://msdn.microsoft.com/a3c66874-b2a8-485a-9b03-bc28db74ca6c">ShowScrollBar</a> function to hide the scroll bar. 

If the call to <b>SetScrollRange</b> immediately follows a call to the <a href="https://msdn.microsoft.com/068d874d-ea9e-4953-93b3-9e90141d4e50">SetScrollPos</a> function, the 
				<i>bRedraw</i> parameter in <b>SetScrollPos</b> must be zero to prevent the scroll bar from being drawn twice. 

The default range for a standard scroll bar is 0 through 100. The default range for a scroll bar control is empty (both the 
				<i>nMinPos</i> and 
				<i>nMaxPos</i> parameter values are zero). The difference between the values specified by the 
				<i>nMinPos</i> and 
				<i>nMaxPos</i> parameters must not be greater than the value of MAXLONG. 

Because the messages that indicate scroll bar position, 
				<a href="https://msdn.microsoft.com/197e522f-defd-4356-8521-5b5dfda596da">WM_HSCROLL</a> and 
				<a href="https://msdn.microsoft.com/495733b8-1aac-4ff7-b0be-15f14581f41c">WM_VSCROLL</a>, are limited to 16 bits of position data, applications that rely solely on those messages for position data have a practical maximum value of 65,535 for the <b>SetScrollRange</b> function's 
				<i>nMaxPos</i> parameter. 

However, because the <a href="https://msdn.microsoft.com/a45af17c-df18-4156-be8b-868fc4cb0696">SetScrollInfo</a>, <a href="https://msdn.microsoft.com/068d874d-ea9e-4953-93b3-9e90141d4e50">SetScrollPos</a>, <b>SetScrollRange</b>, <a href="https://msdn.microsoft.com/c4bd075b-b4fd-44cf-ba51-b9d8a95a5152">GetScrollInfo</a>, <a href="https://msdn.microsoft.com/8d8c43df-c444-4c0a-82e5-bdc568161561">GetScrollPos</a>, and <a href="https://msdn.microsoft.com/883a7d53-7dc0-4b0c-bcda-e1f022dad12a">GetScrollRange</a> functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the 
				<a href="https://msdn.microsoft.com/197e522f-defd-4356-8521-5b5dfda596da">WM_HSCROLL</a> and 
				<a href="https://msdn.microsoft.com/495733b8-1aac-4ff7-b0be-15f14581f41c">WM_VSCROLL</a> messages. See <b>GetScrollInfo</b> for a description of the technique. 

If the <i>nBar</i> parameter is SB_CTL and the window specified by the <i>hWnd</i> parameter is not a system scroll bar control, the system sends the <a href="https://msdn.microsoft.com/9cf84354-3944-4c10-9b59-39427b840868">SBM_SETRANGE</a> message to the window to set scroll bar information.  This allows <b>SetScrollRange</b> to operate on a custom control that mimics a scroll bar.  If the window does not handle the <b>SBM_SETRANGE</b> message, the <b>SetScrollRange</b> function fails.


#### Examples




			For an example, see <a href="https://msdn.microsoft.com/377fb2cc-5b46-481a-8222-9291e504ae2c">Using the Owner-Display Clipboard Format</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c4bd075b-b4fd-44cf-ba51-b9d8a95a5152">GetScrollInfo</a>



<a href="https://msdn.microsoft.com/8d8c43df-c444-4c0a-82e5-bdc568161561">GetScrollPos</a>



<a href="https://msdn.microsoft.com/883a7d53-7dc0-4b0c-bcda-e1f022dad12a">GetScrollRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a45af17c-df18-4156-be8b-868fc4cb0696">SetScrollInfo</a>



<a href="https://msdn.microsoft.com/068d874d-ea9e-4953-93b3-9e90141d4e50">SetScrollPos</a>



<a href="https://msdn.microsoft.com/a3c66874-b2a8-485a-9b03-bc28db74ca6c">ShowScrollBar</a>
 

 

