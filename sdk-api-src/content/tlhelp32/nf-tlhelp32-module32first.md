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

# Module32First function


## -description


Retrieves information about the first module associated with a process.


## -parameters




### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a> function.


### -param lpme [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/305fab35-625c-42e3-a434-e2513e4c8870">MODULEENTRY32</a> structure.


## -returns



Returns <b>TRUE</b> if the first entry of the module list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function if no modules exist or the snapshot does not contain module information.




## -remarks



The calling application must set the <b>dwSize</b> member of 
<a href="https://msdn.microsoft.com/305fab35-625c-42e3-a434-e2513e4c8870">MODULEENTRY32</a> to the size, in bytes, of the structure.

To retrieve information about other modules associated with the specified process, use the 
<a href="https://msdn.microsoft.com/88ec1af4-bae7-4cd7-b830-97a98fb337f4">Module32Next</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/8efe1e13-6222-496a-bff3-90f53b03c750">Traversing the Module List</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a>



<a href="https://msdn.microsoft.com/305fab35-625c-42e3-a434-e2513e4c8870">MODULEENTRY32</a>



<a href="https://msdn.microsoft.com/1b539e2f-1326-42aa-af58-ffd7e2833b9b">Module Walking</a>



<a href="https://msdn.microsoft.com/88ec1af4-bae7-4cd7-b830-97a98fb337f4">Module32Next</a>



<a href="https://msdn.microsoft.com/83732bd6-f4cf-409d-ad17-86503d408dc3">Tool Help Functions</a>
 

 

