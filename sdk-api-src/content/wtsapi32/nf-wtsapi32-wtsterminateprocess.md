---
UID: NF:wtsapi32.WTSTerminateProcess
title: WTSTerminateProcess function
author: windows-sdk-content
description: Terminates the specified process on the specified Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\wtsterminateprocess.htm
old-project: termserv
ms.assetid: 38036657-4e65-4100-893a-e35cf0b71e0d
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: WTSTerminateProcess, WTSTerminateProcess function [Remote Desktop Services], _win32_wtsterminateprocess, termserv.wtsterminateprocess, wtsapi32/WTSTerminateProcess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSTerminateProcess
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSTerminateProcess function


## -description


Terminates the specified process on the specified Remote Desktop Session Host (RD Session Host) server.


## -parameters




### -param hServer [in]

Handle to an RD Session Host server. Specify a handle opened by the 
<a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a> function, or specify WTS_CURRENT_SERVER_HANDLE to indicate the RD Session Host server on which your application is running.


### -param ProcessId [in]

Specifies the process identifier of the process to terminate.


### -param ExitCode [in]

Specifies the exit code for the terminated process.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a>
 

 

