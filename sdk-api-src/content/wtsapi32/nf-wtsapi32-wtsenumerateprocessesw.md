---
UID: NF:wtsapi32.WTSEnumerateProcessesW
title: WTSEnumerateProcessesW function
author: windows-sdk-content
description: Retrieves information about the active processes on a specified Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\wtsenumerateprocesses.htm
tech.root: TermServ
ms.assetid: ddfae294-2e7c-416e-b328-76d011b4af39
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WTSEnumerateProcesses, WTSEnumerateProcesses function [Remote Desktop Services], WTSEnumerateProcessesA, WTSEnumerateProcessesW, _win32_wtsenumerateprocesses, termserv.wtsenumerateprocesses, wtsapi32/WTSEnumerateProcesses, wtsapi32/WTSEnumerateProcessesA, wtsapi32/WTSEnumerateProcessesW
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSEnumerateProcessesW (Unicode) and WTSEnumerateProcessesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSEnumerateProcesses
 - WTSEnumerateProcessesA
 - WTSEnumerateProcessesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WTSEnumerateProcessesW function


## -description


Retrieves information about the active 
    processes on a specified Remote Desktop Session Host (RD Session Host) server.


## -parameters




### -param hServer [in]

Handle to an RD Session Host server. Specify a handle opened by the 
      <a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a> function, or specify 
      <b>WTS_CURRENT_SERVER_HANDLE</b> to indicate the RD Session Host server on which your application is 
      running.


### -param Reserved [in]

Reserved; must be zero.


### -param Version [in]

Specifies the version of the enumeration request. Must be 1.


### -param ppProcessInfo [out]

Pointer to a variable that receives a pointer to an array of 
      <a href="https://msdn.microsoft.com/5df01ad8-71fd-4831-8eba-1d6cabd61348">WTS_PROCESS_INFO</a> structures. Each structure 
      in the array contains information about an active process on the specified RD Session Host server. To free the returned 
      buffer, call the <a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a> function.


### -param pCount [out]

Pointer to a variable that receives the number of <b>WTS_PROCESS_INFO</b> 
      structures returned in the <i>ppProcessInfo</i> buffer.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The caller must be a member of the Administrators group to enumerate processes that are running under a 
    different user's context.




## -see-also




<a href="https://msdn.microsoft.com/5df01ad8-71fd-4831-8eba-1d6cabd61348">WTS_PROCESS_INFO</a>
 

 

