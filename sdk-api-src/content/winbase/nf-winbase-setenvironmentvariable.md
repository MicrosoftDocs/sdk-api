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

# SetEnvironmentVariable function


## -description


Sets the contents of the specified environment variable for the current process.


## -parameters




### -param lpName [in]

The name of the environment variable. The operating system creates the environment variable if it does not exist and <i>lpValue</i> is not NULL.


### -param lpValue [in, optional]

The contents of the environment variable. The maximum size of a user-defined environment variable is 32,767 characters. For more information, see 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543043">Environment Variables</a>.

<b>Windows Server 2003 and Windows XP:  </b>The total size of the environment block for a process may not exceed 32,767 characters.

If this parameter is NULL, the variable is deleted from the current process's environment.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function has no effect on the system environment variables or the environment variables of other processes.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/b428688c-7b16-48c7-8d89-55d066496d1c">Changing Environment Variables</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543043">Environment Variables</a>



<a href="https://msdn.microsoft.com/1d4cc328-12e6-4aae-9f58-58675116ad54">GetEnvironmentVariable</a>
 

 

