---
UID: NF:winuser.SetScrollInfo
title: SetScrollInfo function
author: windows-sdk-content
description: The SetScrollInfo function sets the parameters of a scroll bar, including the minimum and maximum scrolling positions, the page size, and the position of the scroll box (thumb). The function also redraws the scroll bar, if requested.
old-location: controls\SetScrollInfo.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\setscrollinfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SB_CTL, SB_HORZ, SB_VERT, SIF_DISABLENOSCROLL, SIF_PAGE, SIF_POS, SIF_RANGE, SetScrollInfo, SetScrollInfo function [Windows Controls], _win32_SetScrollInfo, _win32_SetScrollInfo_cpp, controls.SetScrollInfo, controls._win32_SetScrollInfo, winuser/SetScrollInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
 - SetScrollInfo
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetScrollInfo function


## -description


The <b>SetScrollInfo</b> function sets the parameters of a scroll bar, including the minimum and maximum scrolling positions, the page size, and the position of the scroll box (thumb). The function also redraws the scroll bar, if requested.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a scroll bar control or a window with a standard scroll bar, depending on the value of the 
					<i>fnBar</i> parameter. 


### -param nBar [in]

Type: <b>int</b>

Specifies the type of scroll bar for which to set parameters. This parameter can be one of the following values. 

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
Sets the parameters of a scroll bar control. The 
						<i>hwnd</i> parameter must be the handle to the scroll bar control. 

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Sets the parameters of the window's standard horizontal scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Sets the parameters of the window's standard vertical scroll bar. 

</td>
</tr>
</table>
 


### -param lpsi [in]

Type: <b>LPCSCROLLINFO</b>

Pointer to a <a href="https://msdn.microsoft.com/abb0d18e-81b5-422c-b6e6-318a2d1d11a4">SCROLLINFO</a> structure. Before calling <b>SetScrollInfo</b>, set the 
					<b>cbSize</b> member of the structure to 
					<b>sizeof</b>(<b>SCROLLINFO</b>), set the 
					<b>fMask</b> member to indicate the parameters to set, and specify the new parameter values in the appropriate members.

The 
					<b>fMask</b> member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SIF_DISABLENOSCROLL"></a><a id="sif_disablenoscroll"></a><dl>
<dt><b>SIF_DISABLENOSCROLL</b></dt>
</dl>
</td>
<td width="60%">
Disables the scroll bar instead of removing it, if the scroll bar's new parameters make the scroll bar unnecessary.

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_PAGE"></a><a id="sif_page"></a><dl>
<dt><b>SIF_PAGE</b></dt>
</dl>
</td>
<td width="60%">
Sets the scroll page to the value specified in the 
						<b>nPage</b> member of the <a href="https://msdn.microsoft.com/abb0d18e-81b5-422c-b6e6-318a2d1d11a4">SCROLLINFO</a> structure pointed to by 
						<i>lpsi</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_POS"></a><a id="sif_pos"></a><dl>
<dt><b>SIF_POS</b></dt>
</dl>
</td>
<td width="60%">
Sets the scroll position to the value specified in the 
						<b>nPos</b> member of the <a href="https://msdn.microsoft.com/abb0d18e-81b5-422c-b6e6-318a2d1d11a4">SCROLLINFO</a> structure pointed to by <i>lpsi</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="SIF_RANGE"></a><a id="sif_range"></a><dl>
<dt><b>SIF_RANGE</b></dt>
</dl>
</td>
<td width="60%">
Sets the scroll range to the value specified in the 
						<b>nMin</b> and 
						<b>nMax</b> members of the <a href="https://msdn.microsoft.com/abb0d18e-81b5-422c-b6e6-318a2d1d11a4">SCROLLINFO</a> structure pointed to by 
						<i>lpsi</i>.

</td>
</tr>
</table>
 


### -param redraw [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Specifies whether the scroll bar is redrawn to reflect the changes to the scroll bar. If this parameter is <b>TRUE</b>, the scroll bar is redrawn, otherwise, it is not redrawn. 


## -returns



Type: <b>int</b>

The return value is the current position of the scroll box. 




## -remarks



The <b>SetScrollInfo</b> function performs range checking on the values specified by the 
				<b>nPage</b> and 
				<b>nPos</b> members of the <a href="https://msdn.microsoft.com/abb0d18e-81b5-422c-b6e6-318a2d1d11a4">SCROLLINFO</a> structure. The 
				<b>nPage</b> member must specify a value from 0 to 
				<b>nMax</b> - 
				<b>nMin</b> +1. The 
				<b>nPos</b> member must specify a value between 
				<b>nMin</b> and 
				<b>nMax</b> - 
				<b>max</b>(
				<b>nPage</b>– 1, 0). If either value is beyond its range, the function sets it to a value that is just within the range. 

If the <i>fnBar</i> parameter is SB_CTL and the window specified by the <i>hwnd</i> parameter is not a system scroll bar control, the system sends the <a href="https://msdn.microsoft.com/e0e42a81-67be-4d40-88c8-77398b068617">SBM_SETSCROLLINFO</a> message to the window to set scroll bar information (The system can optimize the message to <a href="https://msdn.microsoft.com/6b3c16ba-1cdf-41ff-8546-ba98477af334">SBM_SETPOS</a> or <a href="https://msdn.microsoft.com/9cf84354-3944-4c10-9b59-39427b840868">SBM_SETRANGE</a> if the request is solely for the position or range).  This allows <b>SetScrollInfo</b> to operate on a custom control that mimics a scroll bar.  If the window does not handle <b>SBM_SETSCROLLINFO</b> (or the optimized <b>SBM_SETPOS</b> message or <b>SBM_SETRANGE</b> message), then the <b>SetScrollInfo</b> function fails.

For an example, see <a href="Using_Scroll_Bars.htm">Scrolling Text with the WM_PAINT Message</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4bd075b-b4fd-44cf-ba51-b9d8a95a5152">GetScrollInfo</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/abb0d18e-81b5-422c-b6e6-318a2d1d11a4">SCROLLINFO</a>
 

 

