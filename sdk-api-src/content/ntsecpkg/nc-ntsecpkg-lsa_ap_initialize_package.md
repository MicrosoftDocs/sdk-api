---
UID: NC:ntsecpkg.LSA_AP_INITIALIZE_PACKAGE
title: LSA_AP_INITIALIZE_PACKAGE (ntsecpkg.h)
author: windows-sdk-content
description: Called once by the Local Security Authority (LSA) during system initialization to provide the authentication package a chance to initialize itself.
old-location: security\lsaapinitializepackage.htm
tech.root: SecAuthN
ms.assetid: 1fed5a5e-5dc1-4b59-aa28-bd1395a27742
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LSA_AP_INITIALIZE_PACKAGE, LSA_AP_INITIALIZE_PACKAGE callback, LsaApInitializePackage, LsaApInitializePackage callback function [Security], _lsa_lsaapinitializepackage, ntsecpkg/LsaApInitializePackage, security.lsaapinitializepackage
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - LsaApInitializePackage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LSA_AP_INITIALIZE_PACKAGE callback function


## -description


Called once by the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) during system initialization to provide the authentication package a chance to initialize itself.


## -parameters




### -param AuthenticationPackageId [in]

The identifier the LSA has assigned to the authentication package.


### -param LsaDispatchTable [in]

Pointer to an 
<a href="https://msdn.microsoft.com/2e144ce0-e8c9-457a-8b12-7d21dda6adf3">LSA_DISPATCH_TABLE</a> structure that contains the addresses of LSA functions that can be called by authentication packages. Your custom authentication package should save this information if it requires any of the functions described in 
<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">LSA Functions Called by Authentication Packages</a>.


### -param Database [in, optional]

This parameter is not used; it is <b>NULL</b>.


### -param Confidentiality [in, optional]

This parameter is not used; it is <b>NULL</b>.


### -param *AuthenticationPackageName [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/4ae4160f-bcad-41d9-8239-91da44702b76">LSA_STRING</a> structure that receives the name of the authentication package. The authentication package is responsible for allocating the structure and the buffer that contains this string (using the 
<a href="https://msdn.microsoft.com/cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba">AllocateLsaHeap</a> function) and returning the address of the structure in this parameter. The buffer will be freed by the LSA when it is no longer needed.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an NTSTATUS error code. For more information, see 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.




## -remarks



This function must be implemented by authentication packages.




## -see-also




<a href="https://msdn.microsoft.com/cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba">AllocateLsaHeap</a>
 

 

