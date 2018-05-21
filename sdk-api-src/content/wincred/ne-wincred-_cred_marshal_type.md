---
UID: NE:wincred._CRED_MARSHAL_TYPE
title: "_CRED_MARSHAL_TYPE"
author: windows-driver-content
description: Specifies the types of credential to be marshaled by CredMarshalCredential or unmarshaled by CredUnmarshalCredential.
old-location: security\cred_marshal_type.htm
old-project: SecAuthN
ms.assetid: 612fdd6f-2b4c-4f41-a00b-250f90eb85d3
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PCRED_MARSHAL_TYPE, CRED_MARSHAL_TYPE, CRED_MARSHAL_TYPE enumeration [Security], CertCredential, PCRED_MARSHAL_TYPE, PCRED_MARSHAL_TYPE enumeration pointer [Security], UsernameTargetCredential, _CRED_MARSHAL_TYPE, _cred_cred_marshal_type, security.cred_marshal_type, wincred/CRED_MARSHAL_TYPE, wincred/CertCredential, wincred/PCRED_MARSHAL_TYPE, wincred/UsernameTargetCredential"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CRED_MARSHAL_TYPE, *PCRED_MARSHAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinCred.h
api_name:
-	CRED_MARSHAL_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRED_MARSHAL_TYPE enumeration


## -description


The <b>CRED_MARSHAL_TYPE</b> enumeration specifies the types of credential to be marshaled by <a href="https://msdn.microsoft.com/20a1d54b-04a7-4b0a-88e4-1970d1f71502">CredMarshalCredential</a> or unmarshaled by <a href="https://msdn.microsoft.com/65757235-d92c-479f-8e2b-1f8d8564792b">CredUnmarshalCredential</a>.


## -enum-fields




### -field CertCredential

Specifies that the credential is a certificate reference described by a <a href="https://msdn.microsoft.com/acaa94c3-0562-420a-95c7-44a71374d5ea">CERT_CREDENTIAL_INFO</a> structure.


### -field UsernameTargetCredential

Specifies that the credential is a reference to a CRED_FLAGS_USERNAME_TARGET credential described by a <a href="https://msdn.microsoft.com/1cb56a85-fafd-4471-b0e9-660ac0dc0219">USERNAME_TARGET_CREDENTIAL_INFO</a> structure.


### -field BinaryBlobCredential


### -field UsernameForPackedCredentials



