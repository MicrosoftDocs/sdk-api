---
UID: NC:ntsecpkg.SpMarshallSupplementalCredsFn
title: SpMarshallSupplementalCredsFn
author: windows-driver-content
description: Converts supplemental credentials from a public format into a format suitable for local procedure calls.
old-location: security\spmarshallsupplementalcreds.htm
old-project: SecAuthN
ms.assetid: 64792843-5129-4a71-b88b-b4caf495a567
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: SpMarshallSupplementalCreds, SpMarshallSupplementalCreds function [Security], SpMarshallSupplementalCredsFn, _ssp_spmarshallsupplementalcreds, ntsecpkg/SpMarshallSupplementalCreds, security.spmarshallsupplementalcreds
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
-	SpMarshallSupplementalCreds
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SpMarshallSupplementalCredsFn callback function


## -description


The <b>SpMarshallSupplementalCreds</b> function converts <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">supplemental credentials</a> from a public format into a format suitable for local procedure calls.


## -parameters




### -param CredentialSize [in]

Specifies the size of the supplemental credentials.


### -param Credentials [in]

Pointer to the supplemental credentials.


### -param MarshalledCredSize [out]

Pointer to the size of the <i>MarshalledCreds</i> buffer.


### -param *MarshalledCreds [out]

Pointer that receives the address of the buffer containing the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">serialized</a> credentials. Allocate the memory for this buffer by calling the 
<a href="https://msdn.microsoft.com/cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba">AllocateHeap</a> function.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



SSP/APs must implement the <b>SpMarshallSupplementalCreds</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpMarshallSupplementalCreds</b> function is available in the 
<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/8e97ea0e-42f5-4641-83d7-3858c533479c">AllocateHeap</a>



<a href="https://msdn.microsoft.com/2b3fc6d1-2f55-4053-9271-f5cb5c318555">SECPKG_USER_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a>
 

 

