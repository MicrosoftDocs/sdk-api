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

# _FILE_SEGMENT_ELEMENT structure


## -description


Union that contains a 64-bit value that points to a page of data. This is used by 
    the <a href="https://msdn.microsoft.com/4ed7c47b-d40b-4016-8550-0af17ee9e86d">ReadFileScatter</a> and 
    <a href="https://msdn.microsoft.com/9590eabb-6e85-406e-8101-e67f87e6850b">WriteFileGather</a> functions.


## -struct-fields




### -field Buffer

<b>PVOID64</b> representation of 64-bit value.

Assigning a pointer to the <b>Buffer</b> member will sign-extend the value if the code is 
      compiled as 32-bits; this can break 32-bit large-address aware applications running on systems configured with 
      <a href="https://msdn.microsoft.com/991eb86f-9e6f-4084-8b6f-f979e42104b5">4-Gigabyte Tuning</a> or running under WOW64 on 64-bit 
      Windows. Therefore, use the <b>PtrToPtr64</b> macro when assigning pointers to the 
      <b>Buffer</b> member.


### -field Alignment

<b>ULONGLONG</b> representation of 64-bit value.


## -see-also




<a href="https://msdn.microsoft.com/406d5c0f-b49a-4075-ac3e-c5b55a0c3fe9">File Management Structures</a>



<a href="https://msdn.microsoft.com/4ed7c47b-d40b-4016-8550-0af17ee9e86d">ReadFileScatter</a>



<a href="https://msdn.microsoft.com/9590eabb-6e85-406e-8101-e67f87e6850b">WriteFileGather</a>
 

 

