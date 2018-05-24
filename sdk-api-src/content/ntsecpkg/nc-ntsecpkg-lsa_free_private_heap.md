---
UID: NC:ntsecpkg.LSA_FREE_PRIVATE_HEAP
title: LSA_FREE_PRIVATE_HEAP
author: windows-driver-content
description: Frees memory that was allocated by using the AllocatePrivateHeap function.
old-location: security\freeprivateheap.htm
old-project: SecAuthN
ms.assetid: f1ca1450-c59c-4c0f-b68b-373f1a7c70da
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: FreePrivateHeap, FreePrivateHeap function [Security], LSA_FREE_PRIVATE_HEAP, ntsecpkg/FreePrivateHeap, security.freeprivateheap
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
-	FreePrivateHeap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LSA_FREE_PRIVATE_HEAP callback function


## -description


Frees memory that was allocated by using the <a href="https://msdn.microsoft.com/956e7aaf-e8b3-4db5-945a-b579f946b769">AllocatePrivateHeap</a> function.


## -parameters




### -param Base [in]

A pointer to the memory to be freed.


## -returns



This function does not return a value.




## -remarks



A pointer to the <b>FreePrivateHeap</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

