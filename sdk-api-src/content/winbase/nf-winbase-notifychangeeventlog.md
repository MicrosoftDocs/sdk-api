---
UID: NF:winbase.NotifyChangeEventLog
title: NotifyChangeEventLog function (winbase.h)
author: windows-sdk-content
description: Enables an application to receive notification when an event is written to the specified event log.
old-location: base\notifychangeeventlog.htm
tech.root: EventLog
ms.assetid: 12b9a7bf-2aad-48b7-8cfd-a72b353ba2b2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NotifyChangeEventLog, NotifyChangeEventLog function, _win32_notifychangeeventlog, base.notifychangeeventlog, winbase/NotifyChangeEventLog
ms.topic: function
req.header: winbase.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
 - NotifyChangeEventLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NotifyChangeEventLog function


## -description


Enables an application to receive notification when an event is written to the specified event log. When the event is written to the log, the specified event object is set to the signaled state.


## -parameters




### -param hEventLog [in]

A handle to an event log. The 
<a href="https://msdn.microsoft.com/6cd8797a-aeaf-4603-b43c-b1ff45b6200a">OpenEventLog</a>  function returns this handle.


### -param hEvent [in]

A handle to a manual-reset or auto-reset event object. Use the 
<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function to create the event object.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>NotifyChangeEventLog</b> function does not work with remote handles. If the <i>hEventLog</i> parameter is the handle to an event log on a remote computer, <b>NotifyChangeEventLog</b> returns zero, and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INVALID_HANDLE</b>.

If the thread is not waiting on the event when the system calls <a href="https://msdn.microsoft.com/b3cfe15a-1a0e-4c29-8840-032e56404400">PulseEvent</a>, the thread will not receive the notification. Therefore, you should create a separate thread to wait for notifications.

The system will continue to notify you of changes until you close the handle to the event log. To close the event log, use the 
<a href="https://msdn.microsoft.com/cb98a0cf-8ee9-4d78-8508-efae1d43a91d">CloseEventLog</a> or 
<a href="https://msdn.microsoft.com/f5d1f4b0-5320-4aec-a129-cafff6f1fed1">DeregisterEventSource</a> function.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3200d666-d927-4198-b1f6-1636971f5f07">Receiving Event Notification</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cb98a0cf-8ee9-4d78-8508-efae1d43a91d">CloseEventLog</a>



<a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a>



<a href="https://msdn.microsoft.com/f5d1f4b0-5320-4aec-a129-cafff6f1fed1">DeregisterEventSource</a>



<a href="https://msdn.microsoft.com/fd5c12ec-3a3d-4b75-a573-0b27ae7a890b">Event Logging Functions</a>



<a href="https://msdn.microsoft.com/6cd8797a-aeaf-4603-b43c-b1ff45b6200a">OpenEventLog</a>
 

 

