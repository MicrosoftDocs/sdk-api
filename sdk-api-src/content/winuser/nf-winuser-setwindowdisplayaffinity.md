---
UID: NF:winuser.SetWindowDisplayAffinity
title: SetWindowDisplayAffinity function (winuser.h)
description: Stores the display affinity setting in kernel mode on the hWnd associated with the window.
helpviewer_keywords: ["SetWindowDisplayAffinity","SetWindowDisplayAffinity function [Windows and Messages]","_win32_SetWindowDisplayAffinity","_win32_setwindowdisplayaffinity_cpp","winmsg.setwindowdisplayaffinity","winui._win32_setwindowdisplayaffinity","winuser/SetWindowDisplayAffinity"]
old-location: winmsg\setwindowdisplayaffinity.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setwindowdisplayaffinity.htm
ms.date: 12/05/2018
ms.keywords: SetWindowDisplayAffinity, SetWindowDisplayAffinity function [Windows and Messages], _win32_SetWindowDisplayAffinity, _win32_setwindowdisplayaffinity_cpp, winmsg.setwindowdisplayaffinity, winui._win32_setwindowdisplayaffinity, winuser/SetWindowDisplayAffinity
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - SetWindowDisplayAffinity
 - winuser/SetWindowDisplayAffinity
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
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SetWindowDisplayAffinity
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# SetWindowDisplayAffinity function


## -description

Specifies where the content of the window can be displayed.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the top-level window. The window must belong to the current process.

### -param dwAffinity [in]

Type: <b>DWORD</b>

The display affinity setting that specifies where the content of the window can be displayed. 

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WDA_NONE"></a><a id="wda_none"></a><dl>
<dt><b>WDA_NONE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Imposes no restrictions on where the window can be displayed.
</td>
</tr>
<tr>
<td width="40%"><a id="WDA_MONITOR"></a><a id="wda_monitor"></a><dl>
<dt><b>WDA_MONITOR</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The window content is displayed only on a monitor.
Everywhere else, the window appears with no content.
</td>
</tr>
<tr>
<td width="40%"><a id="WDA_EXCLUDEFROMCAPTURE"></a><a id="wda_excludefromcapture"></a><dl>
<dt><b>WDA_EXCLUDEFROMCAPTURE</b></dt>
<dt>0x00000011</dt>
</dl>
</td>
<td width="60%">
The window is displayed only on a monitor.
Everywhere else, the window does not appear at all.

One use for this affinity is for windows that show video recording controls, so that the controls are not included in the capture.

Introduced in Windows 10 Version 2004. See remarks about compatibility regarding previous versions of Windows.
</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the function succeeds, it returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b> when, for example, the function call is made on a non top-level window. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function and <a href="/windows/desktop/api/winuser/nf-winuser-getwindowdisplayaffinity">GetWindowDisplayAffinity</a> are designed to support the window content protection feature that is new to Windows 7. This feature enables applications to protect their own onscreen window content from being captured or copied through a specific set of public operating system features and APIs. However, it works only when the Desktop Window Manager(DWM) is composing the desktop. 		

It is important to note that unlike a security feature or an implementation of Digital Rights Management (DRM), there is no guarantee that using <b>SetWindowDisplayAffinity</b> and <a href="/windows/desktop/api/winuser/nf-winuser-getwindowdisplayaffinity">GetWindowDisplayAffinity</a>, and other necessary functions such as <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmiscompositionenabled">DwmIsCompositionEnabled</a>, will strictly protect windowed content, for example where someone takes a photograph of the screen.

Starting in Windows 10 Version 2004, WDA_EXCLUDEFROMCAPTURE is a supported value. Setting the display affinity to WDA_EXCLUDEFROMCAPTURE on previous version of Windows will behave as if WDA_MONITOR is applied.

## -see-also

[SetWindowDisplayAffinity](/windows/desktop/api/winuser/nf-winuser-setwindowdisplayaffinity), [Windows](/windows/desktop/winmsg/windows)
