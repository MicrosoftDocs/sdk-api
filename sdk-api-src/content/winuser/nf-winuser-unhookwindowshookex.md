---
UID: NF:winuser.UnhookWindowsHookEx
title: UnhookWindowsHookEx function (winuser.h)
description: Removes a hook procedure installed in a hook chain by the SetWindowsHookEx function.
helpviewer_keywords: ["UnhookWindowsHookEx","UnhookWindowsHookEx function [Windows and Messages]","_win32_UnhookWindowsHookEx","_win32_unhookwindowshookex_cpp","winmsg.unhookwindowshookex","winui._win32_unhookwindowshookex","winuser/UnhookWindowsHookEx"]
old-location: winmsg\unhookwindowshookex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookfunctions\unhookwindowshookex.htm
ms.date: 12/05/2018
ms.keywords: UnhookWindowsHookEx, UnhookWindowsHookEx function [Windows and Messages], _win32_UnhookWindowsHookEx, _win32_unhookwindowshookex_cpp, winmsg.unhookwindowshookex, winui._win32_unhookwindowshookex, winuser/UnhookWindowsHookEx
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
 - UnhookWindowsHookEx
 - winuser/UnhookWindowsHookEx
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - UnhookWindowsHookEx
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# UnhookWindowsHookEx function


## -description

Removes a hook procedure installed in a hook chain by the <a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a> function.

## -parameters

### -param hhk [in]

Type: <b>HHOOK</b>

A handle to the hook to be removed. This parameter is a hook handle obtained by a previous call to <a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The hook procedure can be in the state of being called by another thread even after <b>UnhookWindowsHookEx</b> returns. If the hook procedure is not being called concurrently, the hook procedure is removed immediately before <b>UnhookWindowsHookEx</b> returns. 


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-hooks">Monitoring System Events</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/winmsg/hooks">Hooks</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>
