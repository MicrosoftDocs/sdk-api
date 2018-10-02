---
UID: NF:wtsapi32.WTSEnumerateProcessesExA
title: WTSEnumerateProcessesExA function
author: windows-sdk-content
description: Retrieves information about the active processes on the specified Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server.
old-location: termserv\wtsenumerateprocessesex.htm
tech.root: TermServ
ms.assetid: bc8a2550-cf89-4203-b96b-c750c0dff255
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WTSEnumerateProcessesEx, WTSEnumerateProcessesEx function [Remote Desktop Services], WTSEnumerateProcessesExA, WTSEnumerateProcessesExW, termserv.wtsenumerateprocessesex, wtsapi32/WTSEnumerateProcessesEx, wtsapi32/WTSEnumerateProcessesExA, wtsapi32/WTSEnumerateProcessesExW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSEnumerateProcessesExW (Unicode) and WTSEnumerateProcessesExA (ANSI)
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
 - WTSEnumerateProcessesEx
 - WTSEnumerateProcessesExA
 - WTSEnumerateProcessesExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WTSEnumerateProcessesExA function


## -description


Retrieves information about the active 
    processes on the specified Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server.


## -parameters




### -param hServer [in]

A handle to an RD Session Host server. Specify a handle opened by the 
      <a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a> function, or specify 
      <b>WTS_CURRENT_SERVER_HANDLE</b> to indicate the server on which your application is 
      running.


### -param pLevel [in, out]

A pointer to a <b>DWORD</b> variable that, on input, specifies the type of information  to return. To return an array of <a href="https://msdn.microsoft.com/5df01ad8-71fd-4831-8eba-1d6cabd61348">WTS_PROCESS_INFO</a> structures, specify zero. To return an array of <a href="https://msdn.microsoft.com/a678d249-4943-4d2b-9cea-87ce20177c75">WTS_PROCESS_INFO_EX</a> structures, specify one.

If you do not specify a valid value for this parameter, on output, <b>WTSEnumerateProcessesEx</b> sets this parameter to one and returns an error. Otherwise, on output, <b>WTSEnumerateProcessesEx</b> does not change the value of this parameter.


### -param SessionId [in]

The session  for which to enumerate processes. To enumerate processes for all sessions on the server,  specify <b>WTS_ANY_SESSION</b>.


### -param ppProcessInfo [out]

A pointer to a variable that receives a pointer to an array of 
      <a href="https://msdn.microsoft.com/5df01ad8-71fd-4831-8eba-1d6cabd61348">WTS_PROCESS_INFO</a> or <a href="https://msdn.microsoft.com/a678d249-4943-4d2b-9cea-87ce20177c75">WTS_PROCESS_INFO_EX</a> structures. The type of structure is determined by the value passed to the <i>pLevel</i> parameter. Each structure 
      in the array contains information about an active process. When you have finished using the array, free it by calling the <a href="https://msdn.microsoft.com/d84a4fe3-a829-4cf3-b217-157391d0c495">WTSFreeMemoryEx</a> function. You should also set the pointer to <b>NULL</b>.


### -param pCount [out]

A pointer to a variable that receives the number of  
      structures returned in the buffer referenced by the <i>ppProcessInfo</i> parameter.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



The caller must be a member of the Administrators group to enumerate processes that are running under another user session.




## -see-also




<a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a>



<a href="https://msdn.microsoft.com/5df01ad8-71fd-4831-8eba-1d6cabd61348">WTS_PROCESS_INFO</a>



<a href="https://msdn.microsoft.com/a678d249-4943-4d2b-9cea-87ce20177c75">WTS_PROCESS_INFO_EX</a>
 

 

