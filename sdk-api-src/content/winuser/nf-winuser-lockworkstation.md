---
UID: NF:winuser.LockWorkStation
title: LockWorkStation function (winuser.h)
description: Locks the workstation's display.helpviewer_keywords: ["LockWorkStation","LockWorkStation function","_win32_lockworkstation","base.lockworkstation","winuser/LockWorkStation"]
old-location: base\lockworkstation.htm
tech.root: Shutdown
ms.assetid: e0f7f2b9-0fc1-4e76-b5bb-286408240fc6
ms.date: 12/05/2018
ms.keywords: LockWorkStation, LockWorkStation function, _win32_lockworkstation, base.lockworkstation, winuser/LockWorkStation
f1_keywords:
- winuser/LockWorkStation
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
- Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
- LockWorkStation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LockWorkStation function


## -description


Locks the workstation's display. Locking a workstation protects it from unauthorized use.


## -parameters






## -returns



If the function succeeds, the return value is nonzero. Because the function executes asynchronously, a nonzero return value indicates that the operation has been initiated. It does not indicate whether the workstation has been successfully locked.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The 
<b>LockWorkStation</b> function is callable only by processes running on the interactive desktop. In addition, the user must be logged on, and the workstation cannot already be locked.

Common reasons the workstation might not be locked even if the function succeeds include the following: no user is logged on, the workstation is already locked, the process is not running on the interactive desktop, or the request is denied by the Graphical Identification and Authentication (GINA) DLL.

This function has the same result as pressing Ctrl+Alt+Del and clicking <b>Lock Workstation</b>. To unlock the workstation, the user must log in. There is no function you can call to determine whether the workstation is locked. To receive notification when the user logs in, use the <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification">WTSRegisterSessionNotification</a> function to receive <a href="https://docs.microsoft.com/windows/desktop/TermServ/wm-wtssession-change">WM_WTSSESSION_CHANGE</a> messages. You can use session notifications to track the desktop state so you know whether it is possible to interact with the user.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/Shutdown/how-to-lock-the-workstation">How to Lock the Workstation</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Shutdown/system-shutdown-functions">System Shutdown Functions</a>
 

 

