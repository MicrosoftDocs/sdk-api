---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
<a href="authentication_functions.htm">LSA Functions Called by Authentication Packages</a>.


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
 

 

