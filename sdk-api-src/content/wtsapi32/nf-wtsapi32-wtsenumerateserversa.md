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

# WTSEnumerateServersA function


## -description


Returns 
   a list of all Remote Desktop Session Host (RD Session Host) servers within the specified domain.


## -parameters




### -param pDomainName [in]

Pointer to the name of the domain to be queried. If the value of this parameter is 
      <b>NULL</b>, the specified domain is the current domain.


### -param Reserved [in]

Reserved. The value of this parameter must be 0.


### -param Version [in]

Version of the enumeration request. The value of the parameter must be 1.


### -param ppServerInfo

Points to an array of <a href="https://msdn.microsoft.com/c7ba5a94-37ff-408f-9a77-91b07c28b7ce">WTS_SERVER_INFO</a> 
      structures, which contains the returned results of the enumeration. After use, the memory used by this buffer 
      should be freed by calling <a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a>.


### -param pCount

Pointer to a variable that receives the number of 
      <a href="https://msdn.microsoft.com/c7ba5a94-37ff-408f-9a77-91b07c28b7ce">WTS_SERVER_INFO</a> structures returned in the 
      <i>ppServerInfo</i> buffer.


## -returns



If the function succeeds, the return value is a nonzero value.

 If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function will not work if NetBT is disabled.




## -see-also




<a href="https://msdn.microsoft.com/c7ba5a94-37ff-408f-9a77-91b07c28b7ce">WTS_SERVER_INFO</a>
 

 

