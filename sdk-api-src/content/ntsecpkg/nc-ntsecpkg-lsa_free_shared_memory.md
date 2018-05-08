---
UID: NC:ntsecpkg.LSA_FREE_SHARED_MEMORY
title: LSA_FREE_SHARED_MEMORY
author: windows-driver-content
description: The FreeSharedMemory function frees a block of shared memory previously allocated by the AllocateSharedMemory function.
old-location: security\freesharedmemory.htm
old-project: SecAuthN
ms.assetid: def16ef0-4ae7-43c5-99c8-493bdf0c6a97
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: FreeSharedMemory, FreeSharedMemory function [Security], LSA_FREE_SHARED_MEMORY, _ssp_freesharedmemory, ntsecpkg/FreeSharedMemory, security.freesharedmemory
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	FreeSharedMemory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_FREE_SHARED_MEMORY callback function


## -description


The <b>FreeSharedMemory</b> function frees a block of shared memory previously allocated by the 
<a href="https://msdn.microsoft.com/77fdedaf-8931-4412-ab35-bd3de8e78b9a">AllocateSharedMemory</a> function.


## -parameters




### -param SharedMem [in]

Pointer to the shared memory section previously reserved using the 
<a href="https://msdn.microsoft.com/22abafd7-1648-4bea-a0a8-0cb58333fbea">CreateSharedMemory</a> function.


### -param Memory [in]

Pointer to the memory previously allocated from the shared memory section specified by the <i>SharedMem</i> parameter, using the 
<a href="https://msdn.microsoft.com/77fdedaf-8931-4412-ab35-bd3de8e78b9a">AllocateSharedMemory</a> function.


## -returns



This function does not return a value.




## -remarks



A pointer to the <b>FreeSharedMemory</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/77fdedaf-8931-4412-ab35-bd3de8e78b9a">AllocateSharedMemory</a>



<a href="https://msdn.microsoft.com/22abafd7-1648-4bea-a0a8-0cb58333fbea">CreateSharedMemory</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

