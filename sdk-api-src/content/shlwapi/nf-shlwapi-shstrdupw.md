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

# SHStrDupW function


## -description


Makes a copy of a string in newly allocated memory.


## -parameters




### -param psz

TBD


### -param ppwsz [out]

Type: <b>LPTSTR*</b>

A pointer to an allocated Unicode string that contains the result. <b>SHStrDup</b> allocates memory for this string with <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. You should free the string with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> when it is no longer needed.

                    

In the case of failure, this value is NULL.


#### - pszSource [in]

Type: <b>LPCTSTR</b>

A pointer to the null-terminated string to be copied.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.




## -remarks



This function will take either Unicode or ANSI strings as input, but the copied string is always Unicode.

This function uses <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> to allocate memory for the copied string. You must free this memory with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> when it is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/fa77f0b3-8a9b-4221-87e3-9aebff4409fb">StrDup</a>
 

 

