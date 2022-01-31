---
UID: NE:wincred._CRED_MARSHAL_TYPE
title: CRED_MARSHAL_TYPE (wincred.h)
description: Specifies the types of credential to be marshaled by CredMarshalCredential or unmarshaled by CredUnmarshalCredential.
helpviewer_keywords: ["*PCRED_MARSHAL_TYPE","CRED_MARSHAL_TYPE","CRED_MARSHAL_TYPE enumeration [Security]","CertCredential","PCRED_MARSHAL_TYPE","PCRED_MARSHAL_TYPE enumeration pointer [Security]","UsernameTargetCredential","_cred_cred_marshal_type","security.cred_marshal_type","wincred/CRED_MARSHAL_TYPE","wincred/CertCredential","wincred/PCRED_MARSHAL_TYPE","wincred/UsernameTargetCredential"]
old-location: security\cred_marshal_type.htm
tech.root: security
ms.assetid: 612fdd6f-2b4c-4f41-a00b-250f90eb85d3
ms.date: 12/05/2018
ms.keywords: '*PCRED_MARSHAL_TYPE, CRED_MARSHAL_TYPE, CRED_MARSHAL_TYPE enumeration [Security], CertCredential, PCRED_MARSHAL_TYPE, PCRED_MARSHAL_TYPE enumeration pointer [Security], UsernameTargetCredential, _cred_cred_marshal_type, security.cred_marshal_type, wincred/CRED_MARSHAL_TYPE, wincred/CertCredential, wincred/PCRED_MARSHAL_TYPE, wincred/UsernameTargetCredential'
req.header: wincred.h
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
targetos: Windows
req.typenames: CRED_MARSHAL_TYPE, *PCRED_MARSHAL_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRED_MARSHAL_TYPE
 - wincred/_CRED_MARSHAL_TYPE
 - PCRED_MARSHAL_TYPE
 - wincred/PCRED_MARSHAL_TYPE
 - CRED_MARSHAL_TYPE
 - wincred/CRED_MARSHAL_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinCred.h
api_name:
 - CRED_MARSHAL_TYPE
---

# CRED_MARSHAL_TYPE enumeration


## -description

The <b>CRED_MARSHAL_TYPE</b> enumeration specifies the types of credential to be marshaled by <a href="/windows/desktop/api/wincred/nf-wincred-credmarshalcredentiala">CredMarshalCredential</a> or unmarshaled by <a href="/windows/desktop/api/wincred/nf-wincred-credunmarshalcredentiala">CredUnmarshalCredential</a>.

## -enum-fields

### -field CertCredential:1

Specifies that the credential is a certificate reference described by a <a href="/windows/desktop/api/wincred/ns-wincred-cert_credential_info">CERT_CREDENTIAL_INFO</a> structure.

### -field UsernameTargetCredential

Specifies that the credential is a reference to a CRED_FLAGS_USERNAME_TARGET credential described by a <a href="/windows/desktop/api/wincred/ns-wincred-username_target_credential_info">USERNAME_TARGET_CREDENTIAL_INFO</a> structure.

### -field BinaryBlobCredential

### -field UsernameForPackedCredentials

### -field BinaryBlobForSystem
