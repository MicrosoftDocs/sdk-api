---
UID: NC:ntsecpkg.LSA_DELETE_SHARED_MEMORY
title: LSA_DELETE_SHARED_MEMORY
author: windows-driver-content
description: The DeleteSharedMemory function releases a section of memory that is shared by clients and a security package.
old-location: security\deletesharedmemory.htm
old-project: SecAuthN
ms.assetid: 8059ff30-6301-4cf6-9620-2ba765303bb4
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: DeleteSharedMemory, DeleteSharedMemory function [Security], LSA_DELETE_SHARED_MEMORY, _ssp_deletesharedmemory, ntsecpkg/DeleteSharedMemory, security.deletesharedmemory
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
-	DeleteSharedMemory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# LSA_DELETE_SHARED_MEMORY callback


## -description


The <b>DeleteSharedMemory</b> function releases a section of memory that is shared by clients and a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.


## -parameters




### -param SharedMem [in]

Pointer to shared memory previously reserved by the 
<a href="https://msdn.microsoft.com/22abafd7-1648-4bea-a0a8-0cb58333fbea">CreateSharedMemory</a> function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.




## -remarks



The <b>DeleteSharedMemory</b> function releases the shared memory reserved by the 
<a href="https://msdn.microsoft.com/22abafd7-1648-4bea-a0a8-0cb58333fbea">CreateSharedMemory</a> function.

To release shared memory allocated by the 
<a href="https://msdn.microsoft.com/77fdedaf-8931-4412-ab35-bd3de8e78b9a">AllocateSharedMemory</a> function, use the 
<a href="https://msdn.microsoft.com/def16ef0-4ae7-43c5-99c8-493bdf0c6a97">FreeSharedMemory</a> function.

Pointers to these functions are available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/77fdedaf-8931-4412-ab35-bd3de8e78b9a">AllocateSharedMemory</a>



<a href="https://msdn.microsoft.com/22abafd7-1648-4bea-a0a8-0cb58333fbea">CreateSharedMemory</a>



<a href="https://msdn.microsoft.com/def16ef0-4ae7-43c5-99c8-493bdf0c6a97">FreeSharedMemory</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

