---
UID: NC:ntsecpkg.LSA_CREATE_SHARED_MEMORY
title: LSA_CREATE_SHARED_MEMORY
author: windows-driver-content
description: The CreateSharedMemory function creates a section of memory that is shared by client processes and the security package.
old-location: security\createsharedmemory.htm
old-project: SecAuthN
ms.assetid: 22abafd7-1648-4bea-a0a8-0cb58333fbea
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CreateSharedMemory, CreateSharedMemory function [Security], LSA_CREATE_SHARED_MEMORY, _ssp_createsharedmemory, ntsecpkg/CreateSharedMemory, security.createsharedmemory
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
-	CreateSharedMemory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LSA_CREATE_SHARED_MEMORY callback function


## -description


The <b>CreateSharedMemory</b> function creates a section of memory that is shared by client processes and the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.


## -parameters




### -param MaxSize [in]

Specifies the maximum size of the shared memory.


### -param InitialSize [in]

Specifies the initial size of the shared memory.


## -returns



The function returns a pointer to the block of shared memory, or <b>NULL</b> if the block was not reserved.




## -remarks



Creating a shared section for each client is not advisable because it is a resource-intensive operation and may exhaust system resources.

The package's clients can write to shared memory which makes it susceptible to attack. Data in the shared segment should not be trusted.

The pointer returned by the <b>CreateSharedMemory</b> function is required by the 
<a href="https://msdn.microsoft.com/77fdedaf-8931-4412-ab35-bd3de8e78b9a">AllocateSharedMemory</a>, 
<a href="https://msdn.microsoft.com/8059ff30-6301-4cf6-9620-2ba765303bb4">DeleteSharedMemory</a>, and 
<a href="https://msdn.microsoft.com/def16ef0-4ae7-43c5-99c8-493bdf0c6a97">FreeSharedMemory</a> functions.

Use the <a href="https://msdn.microsoft.com/8059ff30-6301-4cf6-9620-2ba765303bb4">DeleteSharedMemory</a> function to release memory reserved by the <b>CreateSharedMemory</b> function.

Pointers to these functions are available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/77fdedaf-8931-4412-ab35-bd3de8e78b9a">AllocateSharedMemory</a>



<a href="https://msdn.microsoft.com/8059ff30-6301-4cf6-9620-2ba765303bb4">DeleteSharedMemory</a>



<a href="https://msdn.microsoft.com/def16ef0-4ae7-43c5-99c8-493bdf0c6a97">FreeSharedMemory</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

