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

# InitializeProcThreadAttributeList function


## -description


Initializes the specified list of attributes for process and thread creation.


## -parameters




### -param lpAttributeList [out, optional]

The attribute list. This parameter can be NULL to determine the buffer size required to support the specified number of attributes.


### -param dwAttributeCount [in]

The count of attributes to be added to the list.


### -param dwFlags

This parameter is reserved and must be zero.


### -param lpSize [in, out]

If <i>lpAttributeList</i> is not NULL, this parameter specifies the size in bytes of the <i>lpAttributeList</i> buffer on input. On output, this parameter receives the size in bytes of the initialized attribute list. 

If <i>lpAttributeList</i> is NULL, this parameter receives the required buffer size in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



First, call this function with the <i>dwAttributeCount</i> parameter set to the maximum number of attributes you will be using and the <i>lpAttributeList</i> to NULL. The function returns the required buffer size in bytes in the <i>lpSize</i> parameter. 

<div class="alert"><b>Note</b>  This initial call will return an error by design. This is expected behavior.</div>
<div> </div>
Allocate enough space for the data in the <i>lpAttributeList</i> buffer and call the function again to initialize the buffer.

To add attributes to the list, call the <a href="https://msdn.microsoft.com/5fc3e04f-9b2a-440c-a9aa-d78d9b25b341">UpdateProcThreadAttribute</a> function. To specify these attributes when creating a process, specify EXTENDED_STARTUPINFO_PRESENT in the <i>dwCreationFlag</i> parameter and a <a href="https://msdn.microsoft.com/61203f57-292d-4ea1-88f4-a3b05012d7a3">STARTUPINFOEX</a> structure in the <i>lpStartupInfo</i> parameter. Note that you can specify the same <b>STARTUPINFOEX</b> structure to multiple child processes.

When you have finished using the list, call the <a href="https://msdn.microsoft.com/806326c8-2f1e-4ab8-a6f6-f84763ddc31f">DeleteProcThreadAttributeList</a> function.




## -see-also




<a href="https://msdn.microsoft.com/806326c8-2f1e-4ab8-a6f6-f84763ddc31f">DeleteProcThreadAttributeList</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/5fc3e04f-9b2a-440c-a9aa-d78d9b25b341">UpdateProcThreadAttribute</a>
 

 

