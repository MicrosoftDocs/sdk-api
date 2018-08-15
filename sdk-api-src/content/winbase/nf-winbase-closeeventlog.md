---
UID: NF:winbase.CloseEventLog
title: CloseEventLog function
author: windows-sdk-content
description: Closes the specified event log.
old-location: base\closeeventlog.htm
old-project: eventlog
ms.assetid: cb98a0cf-8ee9-4d78-8508-efae1d43a91d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CloseEventLog, CloseEventLog function, _win32_closeeventlog, base.closeeventlog, winbase/CloseEventLog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
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
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-MS-Win-AdvAPI32-EventLog-l1-1-0.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
 - CloseEventLog
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CloseEventLog function


## -description


Closes the specified event log.


## -parameters




### -param hEventLog [in, out]

A handle to the event log to be closed. The 
<a href="https://msdn.microsoft.com/6cd8797a-aeaf-4603-b43c-b1ff45b6200a">OpenEventLog</a> or 
<a href="https://msdn.microsoft.com/cfef0912-9d35-44aa-a1d3-f9bb37213ce0">OpenBackupEventLog</a> function returns this handle.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/fd5c12ec-3a3d-4b75-a573-0b27ae7a890b">Event Logging Functions</a>



<a href="https://msdn.microsoft.com/6cd8797a-aeaf-4603-b43c-b1ff45b6200a">OpenEventLog</a>
 

 

