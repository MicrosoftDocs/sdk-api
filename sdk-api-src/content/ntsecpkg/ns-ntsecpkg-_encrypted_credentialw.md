---
UID: NS:ntsecpkg._ENCRYPTED_CREDENTIALW
title: "_ENCRYPTED_CREDENTIALW"
author: windows-driver-content
description: Represents an encrypted credential.
old-location: security\encrypted_credentialw.htm
old-project: SecAuthN
ms.assetid: b350ef3d-5ed5-4355-ae3a-f03fafff2f52
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*PENCRYPTED_CREDENTIALW, ENCRYPTED_CREDENTIALW, ENCRYPTED_CREDENTIALW structure [Security], PENCRYPTED_CREDENTIALW, PENCRYPTED_CREDENTIALW structure pointer [Security], _ENCRYPTED_CREDENTIALW, ntsecpkg/ENCRYPTED_CREDENTIALW, ntsecpkg/PENCRYPTED_CREDENTIALW, security.encrypted_credentialw"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: ENCRYPTED_CREDENTIALW, *PENCRYPTED_CREDENTIALW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecpkg.h
api_name:
-	ENCRYPTED_CREDENTIALW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _ENCRYPTED_CREDENTIALW structure


## -description


Represents an encrypted credential.


## -struct-fields




### -field Cred

A pointer to a <a href="https://msdn.microsoft.com/6361b93c-4441-4a01-bd39-b95c42962497">CREDENTIAL</a> structure that contains the encrypted credential.


### -field ClearCredentialBlobSize

The size, in bytes, of the unencrypted credential.


## -see-also




<a href="https://msdn.microsoft.com/9da22201-884d-4822-a769-c2ce0d36ec73">CrediFreeCredentials</a>



<a href="https://msdn.microsoft.com/b6abfde9-74ac-4af0-b8ab-4f6be937f17f">CrediRead</a>



<a href="https://msdn.microsoft.com/fa5c92be-c74b-4143-8526-b60c25461b8c">CrediReadDomainCredentials</a>



<a href="https://msdn.microsoft.com/19c7fe4d-9c7b-4547-baab-443483deb013">CrediWrite</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

