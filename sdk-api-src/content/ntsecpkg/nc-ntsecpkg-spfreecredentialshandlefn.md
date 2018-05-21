---
UID: NC:ntsecpkg.SpFreeCredentialsHandleFn
title: SpFreeCredentialsHandleFn
author: windows-driver-content
description: Frees credentials acquired by calling the SpAcquireCredentialsHandle function.
old-location: security\spfreecredentialshandle.htm
old-project: SecAuthN
ms.assetid: c8364202-d366-47a2-bc4a-c899588a78db
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: SpFreeCredentialsHandle, SpFreeCredentialsHandle function [Security], SpFreeCredentialsHandleFn, _ssp_spfreecredentialshandle, ntsecpkg/SpFreeCredentialsHandle, security.spfreecredentialshandle
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
-	SpFreeCredentialsHandle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SpFreeCredentialsHandleFn callback function


## -description


Frees <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a> acquired by calling the 
<a href="https://msdn.microsoft.com/d01245d9-fbca-4346-acf5-86ae7f0eb01e">SpAcquireCredentialsHandle</a> function.


## -parameters




### -param CredentialHandle [in]

A handle to the credentials to free.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed. The following  lists a common reason for failure and the error code that the function should return.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
</table>
 




## -remarks



SSP/APs must implement the <b>SpFreeCredentialsHandle</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpFreeCredentialsHandle</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d01245d9-fbca-4346-acf5-86ae7f0eb01e">SpAcquireCredentialsHandle</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

