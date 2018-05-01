---
UID: NC:ntsecpkg.LSA_FREE_LSA_HEAP
title: LSA_FREE_LSA_HEAP
author: windows-driver-content
description: Deallocates heap memory previously allocated by AllocateLsaHeap.
old-location: security\freelsaheap.htm
old-project: SecAuthN
ms.assetid: bd461a23-2501-48c5-8f2f-c6c98383157f
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: FreeLsaHeap, FreeLsaHeap function [Security], LSA_FREE_LSA_HEAP, _lsa_freelsaheap, ntsecpkg/FreeLsaHeap, security.freelsaheap
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
-	FreeLsaHeap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_FREE_LSA_HEAP callback


## -description


Deallocates heap memory previously allocated by 
<a href="https://msdn.microsoft.com/cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba">AllocateLsaHeap</a>.


## -parameters




### -param Base [in]

Pointer to the buffer to be freed.


## -returns



This function does not return a value. However, if the function sets <i>Base</i> to <b>NULL</b>, the buffer was freed. If <i>Base</i> is not <b>NULL</b> after the function call ends, the buffer could not be freed.




## -see-also




<a href="https://msdn.microsoft.com/2e144ce0-e8c9-457a-8b12-7d21dda6adf3">LSA_DISPATCH_TABLE</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>
 

 

