---
UID: NF:winuser.ChildWindowFromPointEx
title: ChildWindowFromPointEx function (winuser.h)
description: Determines which, if any, of the child windows belonging to the specified parent window contains the specified point.
helpviewer_keywords: ["CWP_ALL","CWP_SKIPDISABLED","CWP_SKIPINVISIBLE","CWP_SKIPTRANSPARENT","ChildWindowFromPointEx","ChildWindowFromPointEx function [Windows and Messages]","_win32_ChildWindowFromPointEx","_win32_childwindowfrompointex_cpp","winmsg.childwindowfrompointex","winui._win32_childwindowfrompointex","winuser/ChildWindowFromPointEx"]
old-location: winmsg\childwindowfrompointex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\childwindowfrompointex.htm
ms.date: 12/05/2018
ms.keywords: CWP_ALL, CWP_SKIPDISABLED, CWP_SKIPINVISIBLE, CWP_SKIPTRANSPARENT, ChildWindowFromPointEx, ChildWindowFromPointEx function [Windows and Messages], _win32_ChildWindowFromPointEx, _win32_childwindowfrompointex_cpp, winmsg.childwindowfrompointex, winui._win32_childwindowfrompointex, winuser/ChildWindowFromPointEx
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ChildWindowFromPointEx
 - winuser/ChildWindowFromPointEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - ChildWindowFromPointEx
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
---

# ChildWindowFromPointEx function


## -description

Determines which, if any, 
		of the child windows belonging to the specified parent window contains the specified point. 
		The function can ignore invisible, disabled, and transparent child windows. The search is 
		restricted to immediate child windows. Grandchildren and deeper descendants are not searched.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the parent window.

### -param pt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

A structure that defines the 
				client coordinates (relative to <i>hwndParent</i>) 
				of the point to be checked.

### -param flags [in]

Type: <b>UINT</b>

The child windows to be skipped. This parameter can be one or more of the 
				following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CWP_ALL"></a><a id="cwp_all"></a><dl>
<dt><b>CWP_ALL</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Does not skip any child windows

</td>
</tr>
<tr>
<td width="40%"><a id="CWP_SKIPDISABLED"></a><a id="cwp_skipdisabled"></a><dl>
<dt><b>CWP_SKIPDISABLED</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Skips disabled child windows

</td>
</tr>
<tr>
<td width="40%"><a id="CWP_SKIPINVISIBLE"></a><a id="cwp_skipinvisible"></a><dl>
<dt><b>CWP_SKIPINVISIBLE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Skips invisible child windows

</td>
</tr>
<tr>
<td width="40%"><a id="CWP_SKIPTRANSPARENT"></a><a id="cwp_skiptransparent"></a><dl>
<dt><b>CWP_SKIPTRANSPARENT</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Skips transparent child windows

</td>
</tr>
</table>

## -returns

Type: <b>HWND</b>

The return value is a handle to the first child window that contains 
				the point and meets the criteria specified by <i>uFlags</i>. 
				If the point is within the parent window but not within any child window that 
				meets the criteria, the return value is a handle to the parent window. If the 
				point lies outside the parent window or if the function fails, the return 
				value is <b>NULL</b>.

## -remarks

The system maintains an internal list that contains the handles of the child 
			windows associated with a parent window. The order of the handles in the list 
			depends on the Z order of the child windows. If more than one child window 
			contains the specified point, the system returns a handle to the first window 
			in the list that contains the point and meets the criteria specified by 
			<i>uFlags</i>.

## -see-also

<b>Conceptual</b>



<b>Other Resources</b>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-windowfrompoint">WindowFromPoint</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
