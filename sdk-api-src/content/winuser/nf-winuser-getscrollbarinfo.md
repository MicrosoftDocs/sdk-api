---
UID: NF:winuser.GetScrollBarInfo
title: GetScrollBarInfo function (winuser.h)
description: The GetScrollBarInfo function retrieves information about the specified scroll bar.
helpviewer_keywords: ["GetScrollBarInfo","GetScrollBarInfo function [Windows Controls]","OBJID_CLIENT","OBJID_HSCROLL","OBJID_VSCROLL","_win32_GetScrollBarInfo","_win32_GetScrollBarInfo_cpp","controls.GetScrollBarInfo","controls._win32_GetScrollBarInfo","winuser/GetScrollBarInfo"]
old-location: controls\GetScrollBarInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\getscrollbarinfo.htm
ms.date: 12/05/2018
ms.keywords: GetScrollBarInfo, GetScrollBarInfo function [Windows Controls], OBJID_CLIENT, OBJID_HSCROLL, OBJID_VSCROLL, _win32_GetScrollBarInfo, _win32_GetScrollBarInfo_cpp, controls.GetScrollBarInfo, controls._win32_GetScrollBarInfo, winuser/GetScrollBarInfo
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
targetos: Windows
req.typenames: 
req.redist: Service Pack 6
ms.custom: 19H1
f1_keywords:
 - GetScrollBarInfo
 - winuser/GetScrollBarInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - GetScrollBarInfo
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# GetScrollBarInfo function


## -description

The <b>GetScrollBarInfo</b> function retrieves information about the specified scroll bar.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a window associated with the scroll bar whose information is to be retrieved. If the 
					<i>idObject</i> parameter is OBJID_CLIENT, 
					<i>hwnd</i> is a handle to a scroll bar control. Otherwise, 
					<i>hwnd</i> is a handle to a window created with <a href="/windows/desktop/winmsg/window-styles">WS_VSCROLL</a> and/or <a href="/windows/desktop/winmsg/window-styles">WS_HSCROLL</a> style.

### -param idObject [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

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

Pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-scrollbarinfo">SCROLLBARINFO</a> structure to receive the information. Before calling <b>GetScrollBarInfo</b>, set the 
					<b>cbSize</b> member to 
					<b>sizeof</b>(<b>SCROLLBARINFO</b>).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <i>idObject</i> is OBJID_CLIENT and the window specified by <i>hwnd</i> is not a system scroll bar control, the system sends the <a href="/windows/desktop/Controls/sbm-getscrollbarinfo">SBM_GETSCROLLBARINFO</a> message to the window to obtain scroll bar information.  This allows <b>GetScrollBarInfo</b> to operate on a custom control that mimics a scroll bar.  If the window does not handle the <b>SBM_GETSCROLLBARINFO</b> message, the <b>GetScrollBarInfo</b> function fails.

## -see-also

<a href="/windows/desktop/api/winuser/ns-winuser-scrollbarinfo">SCROLLBARINFO</a>
