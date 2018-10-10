---
UID: NF:winuser.GetScrollBarInfo
title: GetScrollBarInfo function
author: windows-sdk-content
description: The GetScrollBarInfo function retrieves information about the specified scroll bar.
old-location: controls\GetScrollBarInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\getscrollbarinfo.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GetScrollBarInfo, GetScrollBarInfo function [Windows Controls], OBJID_CLIENT, OBJID_HSCROLL, OBJID_VSCROLL, _win32_GetScrollBarInfo, _win32_GetScrollBarInfo_cpp, controls.GetScrollBarInfo, controls._win32_GetScrollBarInfo, winuser/GetScrollBarInfo
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
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetScrollBarInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: Service Pack 6
---

# GetScrollBarInfo function


## -description


The <b>GetScrollBarInfo</b> function retrieves information about the specified scroll bar.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a window associated with the scroll bar whose information is to be retrieved. If the 
					<i>idObject</i> parameter is OBJID_CLIENT, 
					<i>hwnd</i> is a handle to a scroll bar control. Otherwise, 
					<i>hwnd</i> is a handle to a window created with <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">WS_VSCROLL</a> and/or <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">WS_HSCROLL</a> style. 


### -param idObject [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Specifies the scroll bar object. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OBJID_CLIENT"></a><a id="objid_client"></a><dl>
<dt><b>OBJID_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The 
						<i>hwnd</i> parameter is a handle to a scroll bar control.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJID_HSCROLL"></a><a id="objid_hscroll"></a><dl>
<dt><b>OBJID_HSCROLL</b></dt>
</dl>
</td>
<td width="60%">
The horizontal scroll bar of the 
						<i>hwnd</i> window. 

</td>
</tr>
<tr>
<td width="40%"><a id="OBJID_VSCROLL"></a><a id="objid_vscroll"></a><dl>
<dt><b>OBJID_VSCROLL</b></dt>
</dl>
</td>
<td width="60%">
The vertical scroll bar of the 
						<i>hwnd</i> window. 

</td>
</tr>
</table>
 


### -param psbi [out]

Type: <b>PSCROLLBARINFO</b>

Pointer to a <a href="https://msdn.microsoft.com/ae432826-2515-4cab-bb83-7d2894811ab2">SCROLLBARINFO</a> structure to receive the information. Before calling <b>GetScrollBarInfo</b>, set the 
					<b>cbSize</b> member to 
					<b>sizeof</b>(<b>SCROLLBARINFO</b>). 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If <i>idObject</i> is OBJID_CLIENT and the window specified by <i>hwnd</i> is not a system scroll bar control, the system sends the <a href="https://msdn.microsoft.com/db6f704f-99ee-448c-ae7a-dd5a23399fb6">SBM_GETSCROLLBARINFO</a> message to the window to obtain scroll bar information.  This allows <b>GetScrollBarInfo</b> to operate on a custom control that mimics a scroll bar.  If the window does not handle the <b>SBM_GETSCROLLBARINFO</b> message, the <b>GetScrollBarInfo</b> function fails.





## -see-also




<a href="https://msdn.microsoft.com/ae432826-2515-4cab-bb83-7d2894811ab2">SCROLLBARINFO</a>
 

 

