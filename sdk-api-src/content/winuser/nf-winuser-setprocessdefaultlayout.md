---
UID: NF:winuser.SetProcessDefaultLayout
title: SetProcessDefaultLayout function (winuser.h)
description: Changes the default layout when windows are created with no parent or owner only for the currently running process.
helpviewer_keywords: ["LAYOUT_RTL","SetProcessDefaultLayout","SetProcessDefaultLayout function [Windows and Messages]","_win32_SetProcessDefaultLayout","_win32_setprocessdefaultlayout_cpp","winmsg.setprocessdefaultlayout","winui._win32_setprocessdefaultlayout","winuser/SetProcessDefaultLayout"]
old-location: winmsg\setprocessdefaultlayout.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setprocessdefaultlayout.htm
ms.date: 12/05/2018
ms.keywords: LAYOUT_RTL, SetProcessDefaultLayout, SetProcessDefaultLayout function [Windows and Messages], _win32_SetProcessDefaultLayout, _win32_setprocessdefaultlayout_cpp, winmsg.setprocessdefaultlayout, winui._win32_setprocessdefaultlayout, winuser/SetProcessDefaultLayout
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
 - SetProcessDefaultLayout
 - winuser/SetProcessDefaultLayout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SetProcessDefaultLayout
req.apiset: ext-ms-win-ntuser-window-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# SetProcessDefaultLayout function


## -description

Changes the default layout when windows are created with no parent or owner only for the currently running process.

## -parameters

### -param dwDefaultLayout [in]

Type: <b>DWORD</b>

The default process layout. This parameter can be 0 or the following value. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LAYOUT_RTL"></a><a id="layout_rtl"></a><dl>
<dt><b>LAYOUT_RTL</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Sets the default horizontal layout to be right to left.

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The layout specifies how text and graphics are laid out; the default is left to right. The <b>SetProcessDefaultLayout</b> function changes layout to be right to left, which is the standard in Arabic and Hebrew cultures. 

After the <b>LAYOUT_RTL</b> flag is selected, flags normally specifying right or left are reversed. To avoid confusion, consider defining alternate words for standard flags, such as those in the following table.

<table class="clsStd">
<tr>
<th>Standard flag</th>
<th>Suggested alternate name</th>
</tr>
<tr>
<td><b>WS_EX_RIGHT</b></td>
<td><b>WS_EX_TRAILING</b></td>
</tr>
<tr>
<td><b>WS_EX_RTLREADING</b></td>
<td><b>WS_EX_REVERSEREADING</b></td>
</tr>
<tr>
<td><b>WS_EX_LEFTSCROLLBAR</b></td>
<td><b>WS_EX_LEADSCROLLBAR</b></td>
</tr>
<tr>
<td><b>ES_LEFT</b></td>
<td><b>ES_LEAD</b></td>
</tr>
<tr>
<td><b>ES_RIGHT</b></td>
<td><b>ES_TRAIL</b></td>
</tr>
<tr>
<td><b>EC_LEFTMARGIN</b></td>
<td><b>EC_LEADMARGIN</b></td>
</tr>
<tr>
<td><b>EC_RIGHTMARGIN</b></td>
<td><b>EC_TRAILMARGIN</b></td>
</tr>
</table>
 

If using this function with a mirrored window, note that the <b>SetProcessDefaultLayout</b> function does not mirror the whole process and all the device contexts (DCs) created in it. It mirrors only the mirrored window's DCs. To mirror any DC, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-setlayout">SetLayout</a> function.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getprocessdefaultlayout">GetProcessDefaultLayout</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setlayout">SetLayout</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
