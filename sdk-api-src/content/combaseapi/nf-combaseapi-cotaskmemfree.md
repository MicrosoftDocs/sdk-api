---
UID: NF:combaseapi.CoTaskMemFree
title: CoTaskMemFree function
author: windows-sdk-content
description: Frees a block of task memory previously allocated through a call to the CoTaskMemAlloc or CoTaskMemRealloc function.
old-location: com\cotaskmemfree.htm
old-project: com
ms.assetid: 3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: CoTaskMemFree, CoTaskMemFree function [COM], _com_CoTaskMemFree, com.cotaskmemfree, combaseapi/CoTaskMemFree
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: REGCLS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoTaskMemFree
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# CoTaskMemFree function


## -description


Frees a block of task memory previously allocated through a call to the <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> or <a href="https://msdn.microsoft.com/83014a3e-198d-4b4b-91aa-0c0804c8e1bf">CoTaskMemRealloc</a> function.


## -parameters




### -param pv [in, optional]

A pointer to the memory block to be freed. If this parameter is <b>NULL</b>, the function has no effect.


## -returns



This function does not return a value.




## -remarks



The <b>CoTaskMemFree</b> function uses the default OLE allocator.

The number of bytes freed equals the number of bytes that were originally allocated or reallocated. After the call, the memory block pointed to by pv is invalid and can no longer be used.






## -see-also




<a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>



<a href="https://msdn.microsoft.com/83014a3e-198d-4b4b-91aa-0c0804c8e1bf">CoTaskMemRealloc</a>



<a href="https://msdn.microsoft.com/d65411ea-13d5-4932-a757-d897311e9e28">IMalloc::Free</a>
 

 

