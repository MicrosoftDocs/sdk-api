---
UID: NC:ntsecpkg.LSA_PROTECT_MEMORY
title: LSA_PROTECT_MEMORY
author: windows-driver-content
description: Encrypts the specified memory buffer.
old-location: security\lsaprotectmemory.htm
old-project: SecAuthN
ms.assetid: c851fe8b-be22-4966-ab99-f177989cf382
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: LSA_PROTECT_MEMORY, LsaProtectMemory, LsaProtectMemory function [Security], ntsecpkg/LsaProtectMemory, security.lsaprotectmemory
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
-	LsaProtectMemory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_PROTECT_MEMORY callback function


## -description


Encrypts the specified memory buffer.


## -parameters




### -param Buffer [in, out]

On input, a pointer to the buffer to be encrypted. On output, a pointer to the encrypted buffer.


### -param BufferSize [in]

The size, in bytes, of the <i>Buffer</i> buffer.


## -returns



This function does not return a value.




## -remarks



A pointer to the <b>LsaProtectMemory</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

