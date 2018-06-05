---
UID: NC:ntsecpkg.LSA_ALLOCATE_SHARED_MEMORY
title: LSA_ALLOCATE_SHARED_MEMORY
author: windows-sdk-content
description: The AllocateSharedMemory function allocates a block of shared memory from a section of memory previously reserved by a call to the CreateSharedMemory function.
old-location: security\allocatesharedmemory.htm
old-project: SecAuthN
ms.assetid: 77fdedaf-8931-4412-ab35-bd3de8e78b9a
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: AllocateSharedMemory, AllocateSharedMemory function [Security], LSA_ALLOCATE_SHARED_MEMORY, _ssp_allocatesharedmemory, ntsecpkg/AllocateSharedMemory, security.allocatesharedmemory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	AllocateSharedMemory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LSA_ALLOCATE_SHARED_MEMORY callback function


## -description


The <b>AllocateSharedMemory</b> function allocates a block of shared memory from a section of memory previously reserved by a call to the 
<a href="https://msdn.microsoft.com/22abafd7-1648-4bea-a0a8-0cb58333fbea">CreateSharedMemory</a> function.


## -parameters




### -param SharedMem [in]

Pointer to a section of reserved shared memory.


### -param Size [in]

Specifies the amount of shared memory to allocate, in bytes.


## -returns



If the function succeeds, the return value is a pointer to the allocated memory.

If the function fails, the return value is <b>NULL</b>.




## -remarks



Reserve a section of shared memory using the 
<a href="https://msdn.microsoft.com/22abafd7-1648-4bea-a0a8-0cb58333fbea">CreateSharedMemory</a> function. Free a block of memory allocated by <b>AllocateSharedMemory</b> using the 
<a href="https://msdn.microsoft.com/def16ef0-4ae7-43c5-99c8-493bdf0c6a97">FreeSharedMemory</a> function.

A pointer to the <b>AllocateSharedMemory</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/22abafd7-1648-4bea-a0a8-0cb58333fbea">CreateSharedMemory</a>



<a href="https://msdn.microsoft.com/def16ef0-4ae7-43c5-99c8-493bdf0c6a97">FreeSharedMemory</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

