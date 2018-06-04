---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WTS_PROCESS_INFO_EXW structure


## -description


Contains extended information about a process running on a Remote Desktop Session Host (RD Session Host) server. This structure is returned by the <a href="https://msdn.microsoft.com/bc8a2550-cf89-4203-b96b-c750c0dff255">WTSEnumerateProcessesEx</a> function when you set the <i>pLevel</i> parameter to one.


## -struct-fields




### -field SessionId

The Remote Desktop Services session identifier for the session associated with the process.


### -field ProcessId

The process identifier that uniquely identifies the process on the RD Session Host server.


### -field pProcessName

A pointer to a null-terminated string that contains the name of the executable file associated with the process.


### -field pUserSid

A pointer to the user security identifiers (SIDs) in the primary access token of the process. For more 
      information about SIDs and access tokens, see 
      <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a> and 
      <a href="https://msdn.microsoft.com/7cb07bcd-70f4-43dd-8382-320fcff151c7">Security Identifiers</a>.


### -field NumberOfThreads

The number of threads in the process.


### -field HandleCount

The number of handles in the process.


### -field PagefileUsage

The page file usage of the process, in bytes.


### -field PeakPagefileUsage

The peak page file usage of the process, in bytes.


### -field WorkingSetSize

The working set size of the process, in bytes.


### -field PeakWorkingSetSize

The peak working set size of the process, in bytes.


### -field UserTime

The amount of time, in milliseconds, the process has been running in user mode.


### -field KernelTime

The amount of time, in milliseconds, the process has been running in kernel mode.


## -see-also




<a href="https://msdn.microsoft.com/ddfae294-2e7c-416e-b328-76d011b4af39">WTSEnumerateProcesses</a>



<a href="https://msdn.microsoft.com/bc8a2550-cf89-4203-b96b-c750c0dff255">WTSEnumerateProcessesEx</a>



<a href="https://msdn.microsoft.com/5df01ad8-71fd-4831-8eba-1d6cabd61348">WTS_PROCESS_INFO</a>
 

 

