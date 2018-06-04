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

# ReallocADsStr function


## -description


The <b>ReallocADsStr</b> function creates a copy of a Unicode string.


## -parameters




### -param ppStr [out]

Type: <b>LPWSTR*</b>

Pointer to null-terminated Unicode string pointer that receives the allocated string. <b>ReallocADsStr</b> will attempt to free this memory with <a href="https://msdn.microsoft.com/9c8eaac2-1fb4-47f9-8f60-6896073012aa">FreeADsStr</a> before reallocating the string, so this parameter should be initialized to <b>NULL</b> if the memory should not be freed or was not allocated with the <a href="https://msdn.microsoft.com/df98a728-596b-4541-974a-5690e510ad9f">AllocADsMem</a>, <a href="https://msdn.microsoft.com/1e2b6d42-a879-4a53-a2ce-0e841f6b8543">AllocADsStr</a>, <a href="https://msdn.microsoft.com/471b8ae7-d3b6-4dd9-aa00-6e1d3ab278a9">ReallocADsMem</a> or <b>ReallocADsStr</b> function.

The caller must free this memory when it is no longer required by passing this pointer to <a href="https://msdn.microsoft.com/9c8eaac2-1fb4-47f9-8f60-6896073012aa">FreeADsStr</a>.


### -param pStr [in]

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode string that contains the string to copy.


## -returns



Type: <b>BOOL</b>

The function returns <b>TRUE</b> if  successful, otherwise <b>FALSE</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/df98a728-596b-4541-974a-5690e510ad9f">AllocADsMem</a>



<a href="https://msdn.microsoft.com/1e2b6d42-a879-4a53-a2ce-0e841f6b8543">AllocADsStr</a>



<a href="https://msdn.microsoft.com/9c8eaac2-1fb4-47f9-8f60-6896073012aa">FreeADsStr</a>



<a href="https://msdn.microsoft.com/471b8ae7-d3b6-4dd9-aa00-6e1d3ab278a9">ReallocADsMem</a>
 

 

