---
UID: NF:winuser.LockSetForegroundWindow
title: LockSetForegroundWindow function (winuser.h)
description: The foreground process can call the LockSetForegroundWindow function to disable calls to the SetForegroundWindow function.
helpviewer_keywords: ["LSFW_LOCK","LSFW_UNLOCK","LockSetForegroundWindow","LockSetForegroundWindow function [Windows and Messages]","_win32_LockSetForegroundWindow","_win32_locksetforegroundwindow_cpp","winmsg.locksetforegroundwindow","winui._win32_locksetforegroundwindow","winuser/LockSetForegroundWindow"]
old-location: winmsg\locksetforegroundwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\locksetforegroundwindow.htm
ms.date: 12/05/2018
ms.keywords: LSFW_LOCK, LSFW_UNLOCK, LockSetForegroundWindow, LockSetForegroundWindow function [Windows and Messages], _win32_LockSetForegroundWindow, _win32_locksetforegroundwindow_cpp, winmsg.locksetforegroundwindow, winui._win32_locksetforegroundwindow, winuser/LockSetForegroundWindow
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
 - LockSetForegroundWindow
 - winuser/LockSetForegroundWindow
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
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - LockSetForegroundWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# LockSetForegroundWindow function


## -description

The foreground process can call the <b>LockSetForegroundWindow</b> function to disable calls to the <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a> function.

## -parameters

### -param uLockCode [in]

Type: <b>UINT</b>

Specifies whether to enable or disable calls to <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a>. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LSFW_LOCK"></a><a id="lsfw_lock"></a><dl>
<dt><b>LSFW_LOCK</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Disables calls to <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="LSFW_UNLOCK"></a><a id="lsfw_unlock"></a><dl>
<dt><b>LSFW_UNLOCK</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Enables calls to <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a>.

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The system automatically enables calls to <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a> if the user presses the ALT key or takes some action that causes the system itself to change the foreground window (for example, clicking a background window).

This function is provided so applications can prevent other applications from making a foreground change that can interrupt its interaction with the user.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow">AllowSetForegroundWindow</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
