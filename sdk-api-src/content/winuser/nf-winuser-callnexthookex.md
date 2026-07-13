---
UID: NF:winuser.CallNextHookEx
title: CallNextHookEx function (winuser.h)
description: Passes the hook information to the next hook procedure in the current hook chain. A hook procedure can call this function either before or after processing the hook information.
helpviewer_keywords: ["CallNextHookEx","CallNextHookEx function [Windows and Messages]","_win32_CallNextHookEx","_win32_callnexthookex_cpp","winmsg.callnexthookex","winui._win32_callnexthookex","winuser/CallNextHookEx"]
old-location: winmsg\callnexthookex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookfunctions\callnexthookex.htm
ms.date: 12/05/2018
ms.keywords: CallNextHookEx, CallNextHookEx function [Windows and Messages], _win32_CallNextHookEx, _win32_callnexthookex_cpp, winmsg.callnexthookex, winui._win32_callnexthookex, winuser/CallNextHookEx
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
 - CallNextHookEx
 - winuser/CallNextHookEx
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
 - CallNextHookEx
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# CallNextHookEx function


## -description

Passes the hook information to the next hook procedure in the current hook chain. A hook procedure can call this function either before or after processing the hook information.

## -parameters

### -param hhk [in, optional]

Type: <b>HHOOK</b>

This parameter is ignored.

### -param nCode [in]

Type: <b>int</b>

The hook code passed to the current hook procedure. The next hook procedure uses this code to determine how to process the hook information.

### -param wParam [in]

Type: <b>WPARAM</b>

The <i>wParam</i> value passed to the current hook procedure. The meaning of this parameter depends on the type of hook associated with the current hook chain.

### -param lParam [in]

Type: <b>LPARAM</b>

The <i>lParam</i> value passed to the current hook procedure. The meaning of this parameter depends on the type of hook associated with the current hook chain.

## -returns

Type: <b>LRESULT</b>

This value is returned by the next hook procedure in the chain. The current hook procedure must also return this value. The meaning of the return value depends on the hook type. For more information, see the descriptions of the individual hook procedures.

## -remarks

Hook procedures are installed in chains for particular hook types. <b>CallNextHookEx</b> calls the next hook in the chain. 

Calling <b>CallNextHookEx</b> is optional, but it is highly recommended; otherwise, other applications that have installed hooks will not receive hook notifications and may behave incorrectly as a result. You should call <b>CallNextHookEx</b> unless you absolutely need to prevent the notification from being seen by other applications.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/winmsg/hooks">Hooks</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>



[UnhookWindowsHookEx function](nf-winuser-unhookwindowshookex.md)
