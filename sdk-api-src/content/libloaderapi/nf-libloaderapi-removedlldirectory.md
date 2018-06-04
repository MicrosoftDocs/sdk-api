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

# RemoveDllDirectory function


## -description


Removes a directory that was added to the process DLL search path by using 
     <a href="https://msdn.microsoft.com/7eb49bdf-58f9-4520-876b-c8b69bf26b8a">AddDllDirectory</a>.


## -parameters




### -param Cookie [in]

The cookie returned by <a href="https://msdn.microsoft.com/7eb49bdf-58f9-4520-876b-c8b69bf26b8a">AddDllDirectory</a> when the 
      directory was added to the search path.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value 
      is zero. To get extended error information, call 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After <b>RemoveDllDirectory</b> returns, the cookie is 
    no longer valid and should not be used.

<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>To call this function in an application, use the 
      <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> function to retrieve its address from 
      Kernel32.dll. 
      <a href="http://go.microsoft.com/fwlink/p/?linkid=217865">KB2533623</a> must be 
      installed on the target platform.



