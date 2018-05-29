---
UID: NC:ntsecpkg.LSA_ALLOCATE_PRIVATE_HEAP
title: LSA_ALLOCATE_PRIVATE_HEAP
author: windows-sdk-content
description: Allocates memory on the private heap.
old-location: security\allocateprivateheap.htm
old-project: SecAuthN
ms.assetid: 956e7aaf-e8b3-4db5-945a-b579f946b769
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: AllocatePrivateHeap, AllocatePrivateHeap function [Security], LSA_ALLOCATE_PRIVATE_HEAP, ntsecpkg/AllocatePrivateHeap, security.allocateprivateheap
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	AllocatePrivateHeap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LSA_ALLOCATE_PRIVATE_HEAP callback function


## -description


Allocates memory on the private heap.

Memory allocated with this routine must be deallocated with the 
<a href="https://msdn.microsoft.com/f1ca1450-c59c-4c0f-b68b-373f1a7c70da">FreePrivateHeap</a> function.


## -parameters




### -param Length [in]

Number of bytes to allocate from the heap.


## -returns



This function returns a pointer to the allocated heap memory. If memory could not be allocated, the function returns <b>NULL</b>.




## -remarks



A pointer to the <b>AllocatePrivateHeap</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

