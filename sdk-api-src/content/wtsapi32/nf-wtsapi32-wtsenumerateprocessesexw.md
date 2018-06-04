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

# WTSEnumerateProcessesExW function


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


### -param SessionId

TBD


### -param ppProcessInfo [out]

A pointer to a variable that receives a pointer to an array of 
      <a href="https://msdn.microsoft.com/5df01ad8-71fd-4831-8eba-1d6cabd61348">WTS_PROCESS_INFO</a> or <a href="https://msdn.microsoft.com/a678d249-4943-4d2b-9cea-87ce20177c75">WTS_PROCESS_INFO_EX</a> structures. The type of structure is determined by the value passed to the <i>pLevel</i> parameter. Each structure 
      in the array contains information about an active process. When you have finished using the array, free it by calling the <a href="https://msdn.microsoft.com/d84a4fe3-a829-4cf3-b217-157391d0c495">WTSFreeMemoryEx</a> function. You should also set the pointer to <b>NULL</b>.


### -param pCount [out]

A pointer to a variable that receives the number of  
      structures returned in the buffer referenced by the <i>ppProcessInfo</i> parameter.


#### - SessionID [in]

The session  for which to enumerate processes. To enumerate processes for all sessions on the server,  specify <b>WTS_ANY_SESSION</b>.


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
 

 

