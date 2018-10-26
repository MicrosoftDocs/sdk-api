---
UID: NF:winuser.CallNextHookEx
title: CallNextHookEx function
author: windows-sdk-content
description: Passes the hook information to the next hook procedure in the current hook chain. A hook procedure can call this function either before or after processing the hook information.
old-location: winmsg\callnexthookex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookfunctions\callnexthookex.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CallNextHookEx, CallNextHookEx function [Windows and Messages], _win32_CallNextHookEx, _win32_callnexthookex_cpp, winmsg.callnexthookex, winui._win32_callnexthookex, winuser/CallNextHookEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



Type: <strong>Type: <b>LRESULT</b>
</strong>

This value is returned by the next hook procedure in the chain. The current hook procedure must also return this value. The meaning of the return value depends on the hook type. For more information, see the descriptions of the individual hook procedures.




## -remarks



Hook procedures are installed in chains for particular hook types. <b>CallNextHookEx</b> calls the next hook in the chain. 

Calling <b>CallNextHookEx</b> is optional, but it is highly recommended; otherwise, other applications that have installed hooks will not receive hook notifications and may behave incorrectly as a result. You should call <b>CallNextHookEx</b> unless you absolutely need to prevent the notification from being seen by other applications.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632589(v=VS.85).aspx">Hooks</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644990(v=VS.85).aspx">SetWindowsHookEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644993(v=VS.85).aspx">UnhookWindowsHookEx</a>
 

 

