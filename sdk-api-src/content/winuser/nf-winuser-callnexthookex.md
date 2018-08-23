---
UID: NF:winuser.CallNextHookEx
title: CallNextHookEx function
author: windows-sdk-content
description: Passes the hook information to the next hook procedure in the current hook chain. A hook procedure can call this function either before or after processing the hook information.
old-location: winmsg\callnexthookex.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookfunctions\callnexthookex.htm
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: CallNextHookEx, CallNextHookEx function [Windows and Messages], _win32_CallNextHookEx, _win32_callnexthookex_cpp, winmsg.callnexthookex, winui._win32_callnexthookex, winuser/CallNextHookEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



<a href="https://msdn.microsoft.com/987095d7-059f-4eae-925d-6723ab6d524c">Hooks</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/66c96282-528c-4f57-acab-ae03178e4fe9">SetWindowsHookEx</a>



<a href="https://msdn.microsoft.com/0266fc5f-f62f-4bad-99b9-7cd16edb07de">UnhookWindowsHookEx</a>
 

 

