---
UID: NF:winuser.EnableScrollBar
title: EnableScrollBar function (winuser.h)
description: The EnableScrollBar function enables or disables one or both scroll bar arrows.
helpviewer_keywords: ["ESB_DISABLE_BOTH","ESB_DISABLE_DOWN","ESB_DISABLE_LEFT","ESB_DISABLE_LTUP","ESB_DISABLE_RIGHT","ESB_DISABLE_RTDN","ESB_DISABLE_UP","ESB_ENABLE_BOTH","EnableScrollBar","EnableScrollBar function [Windows Controls]","SB_BOTH","SB_CTL","SB_HORZ","SB_VERT","_win32_EnableScrollBar","_win32_EnableScrollBar_cpp","controls.EnableScrollBar","controls._win32_EnableScrollBar","winuser/EnableScrollBar"]
old-location: controls\EnableScrollBar.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\enablescrollbar.htm
ms.date: 12/05/2018
ms.keywords: ESB_DISABLE_BOTH, ESB_DISABLE_DOWN, ESB_DISABLE_LEFT, ESB_DISABLE_LTUP, ESB_DISABLE_RIGHT, ESB_DISABLE_RTDN, ESB_DISABLE_UP, ESB_ENABLE_BOTH, EnableScrollBar, EnableScrollBar function [Windows Controls], SB_BOTH, SB_CTL, SB_HORZ, SB_VERT, _win32_EnableScrollBar, _win32_EnableScrollBar_cpp, controls.EnableScrollBar, controls._win32_EnableScrollBar, winuser/EnableScrollBar
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnableScrollBar
 - winuser/EnableScrollBar
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
 - EnableScrollBar
req.apiset: ext-ms-win-ntuser-misc-l1-2-0 (introduced in Windows 8.1)
---

# EnableScrollBar function


## -description

The <b>EnableScrollBar</b> function enables or disables one or both scroll bar arrows.

## -parameters

### -param hWnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a window or a scroll bar control, depending on the value of the 
					<i>wSBflags</i> parameter.

### -param wSBflags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the scroll bar type. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SB_BOTH"></a><a id="sb_both"></a><dl>
<dt><b>SB_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Enables or disables the arrows on the horizontal and vertical scroll bars associated with the specified window. The 
						<i>hWnd</i> parameter must be the handle to the window.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_CTL"></a><a id="sb_ctl"></a><dl>
<dt><b>SB_CTL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the scroll bar is a scroll bar control. The 
						<i>hWnd</i> must be the handle to the scroll bar control.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_HORZ"></a><a id="sb_horz"></a><dl>
<dt><b>SB_HORZ</b></dt>
</dl>
</td>
<td width="60%">
Enables or disables the arrows on the horizontal scroll bar associated with the specified window. The 
						<i>hWnd</i> parameter must be the handle to the window.

</td>
</tr>
<tr>
<td width="40%"><a id="SB_VERT"></a><a id="sb_vert"></a><dl>
<dt><b>SB_VERT</b></dt>
</dl>
</td>
<td width="60%">
Enables or disables the arrows on the vertical scroll bar associated with the specified window. The 
						<i>hWnd</i> parameter must be the handle to the window.

</td>
</tr>
</table>

### -param wArrows [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies whether the scroll bar arrows are enabled or disabled and indicates which arrows are enabled or disabled. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_BOTH"></a><a id="esb_disable_both"></a><dl>
<dt><b>ESB_DISABLE_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Disables both arrows on a scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_DOWN"></a><a id="esb_disable_down"></a><dl>
<dt><b>ESB_DISABLE_DOWN</b></dt>
</dl>
</td>
<td width="60%">
Disables the down arrow on a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_LEFT"></a><a id="esb_disable_left"></a><dl>
<dt><b>ESB_DISABLE_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Disables the left arrow on a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_LTUP"></a><a id="esb_disable_ltup"></a><dl>
<dt><b>ESB_DISABLE_LTUP</b></dt>
</dl>
</td>
<td width="60%">
Disables the left arrow on a horizontal scroll bar or the up arrow of a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_RIGHT"></a><a id="esb_disable_right"></a><dl>
<dt><b>ESB_DISABLE_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Disables the right arrow on a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_RTDN"></a><a id="esb_disable_rtdn"></a><dl>
<dt><b>ESB_DISABLE_RTDN</b></dt>
</dl>
</td>
<td width="60%">
Disables the right arrow on a horizontal scroll bar or the down arrow of a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_DISABLE_UP"></a><a id="esb_disable_up"></a><dl>
<dt><b>ESB_DISABLE_UP</b></dt>
</dl>
</td>
<td width="60%">
Disables the up arrow on a vertical scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="ESB_ENABLE_BOTH"></a><a id="esb_enable_both"></a><dl>
<dt><b>ESB_ENABLE_BOTH</b></dt>
</dl>
</td>
<td width="60%">
Enables both arrows on a scroll bar.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If the arrows are enabled or disabled as specified, the return value is nonzero.

If the arrows are already in the requested state or an error occurs, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
