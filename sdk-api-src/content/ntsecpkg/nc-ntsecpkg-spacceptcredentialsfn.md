---
UID: NC:ntsecpkg.SpAcceptCredentialsFn
title: SpAcceptCredentialsFn
author: windows-driver-content
description: Called by the Local Security Authority (LSA) to pass the security package any credentials stored for the authenticated security principal.
old-location: security\spacceptcredentials.htm
old-project: SecAuthN
ms.assetid: bb382937-e5d6-452b-b166-505d0c80412c
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: SpAcceptCredentials, SpAcceptCredentials function [Security], SpAcceptCredentialsFn, _ssp_spacceptcredentials, ntsecpkg/SpAcceptCredentials, security.spacceptcredentials
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
-	SpAcceptCredentials
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SpAcceptCredentialsFn callback


## -description


Called by the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) to pass the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> any <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a> stored for the authenticated <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal</a>. This function is called once for each set of credentials stored by the LSA.


## -parameters




### -param LogonType [in]

A 
<a href="https://msdn.microsoft.com/d775d782-9403-47b2-bb43-8f677db49eb9">SECURITY_LOGON_TYPE</a> value indicating the type of logon.


### -param AccountName [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure specifying the name of the logged-on account.


### -param PrimaryCredentials [in]

Pointer to a 
<a href="https://msdn.microsoft.com/e51fd400-6c3c-4861-ab5c-6c1800b12d31">SECPKG_PRIMARY_CRED</a> structure containing the credentials used to logon. This structure can have <b>NULL</b> members.


### -param SupplementalCredentials [in]

Pointer to a 
<a href="https://msdn.microsoft.com/d5a1a986-5343-420d-8553-f1078bbd0e00">SECPKG_SUPPLEMENTAL_CRED</a> structure containing package-specific <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">supplemental credentials</a>.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> should save the credentials so that it can service requests for credentials. For additional information, see the 
<a href="https://msdn.microsoft.com/d01245d9-fbca-4346-acf5-86ae7f0eb01e">SpAcquireCredentialsHandle</a> function.

SSP/APs must implement the <b>SpAcceptCredentials</b> function; unlike other SSP/AP functions the name of the function must be <b>SpAcceptCredentials</b>.

The LSA accesses the <b>SpAcceptCredentials</b> function through the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/e51fd400-6c3c-4861-ab5c-6c1800b12d31">SECPKG_PRIMARY_CRED</a>



<a href="https://msdn.microsoft.com/d5a1a986-5343-420d-8553-f1078bbd0e00">SECPKG_SUPPLEMENTAL_CRED</a>



<a href="https://msdn.microsoft.com/d775d782-9403-47b2-bb43-8f677db49eb9">SECURITY_LOGON_TYPE</a>



<a href="https://msdn.microsoft.com/d01245d9-fbca-4346-acf5-86ae7f0eb01e">SpAcquireCredentialsHandle</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

