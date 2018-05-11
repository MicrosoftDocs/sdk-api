---
UID: NC:ntsecpkg.CredFreeCredentialsFn
title: CredFreeCredentialsFn
author: windows-driver-content
description: Frees memory used to store credentials used by a security package.
old-location: security\credifreecredentials.htm
old-project: SecAuthN
ms.assetid: 9da22201-884d-4822-a769-c2ce0d36ec73
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CredFreeCredentialsFn, CrediFreeCredentials, CrediFreeCredentials function [Security], ntsecpkg/CrediFreeCredentials, security.credifreecredentials
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
-	CrediFreeCredentials
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CredFreeCredentialsFn callback function


## -description


Frees memory used to store credentials used by a  <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.


## -parameters




### -param Count [in]

The number of elements in the <i>Credentials</i> array.


### -param *Credentials [in, out]

A pointer to a pointer that, on input, points to an array of  <a href="https://msdn.microsoft.com/b350ef3d-5ed5-4355-ae3a-f03fafff2f52">ENCRYPTED_CREDENTIALW</a> structures to be freed.


## -returns




						If the function succeeds, the return value is STATUS_SUCCESS.
						

If the function fails, the return value is an NTSTATUS code that indicates the reason it failed.




## -remarks



A pointer to the <b>CrediFreeCredentials</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

