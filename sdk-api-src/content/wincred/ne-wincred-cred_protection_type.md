---
UID: NE:wincred._CRED_PROTECTION_TYPE
title: CRED_PROTECTION_TYPE (wincred.h)

description: Specifies the security context in which credentials are encrypted when using the CredProtect function.
old-location: security\cred_protection_type.htm
tech.root: SecAuthN
ms.assetid: 6d8d8ad6-1b44-4482-a9a2-9c50d522b8d9

ms.date: 12/05/2018
ms.keywords: "*PCRED_PROTECTION_TYPE, CRED_PROTECTION_TYPE, CRED_PROTECTION_TYPE enumeration [Security], CredTrustedProtection, CredUnprotected, CredUserProtection, PCRED_PROTECTION_TYPE, PCRED_PROTECTION_TYPE enumeration pointer [Security], security.cred_protection_type, wincred/CRED_PROTECTION_TYPE, wincred/CredTrustedProtection, wincred/CredUnprotected, wincred/CredUserProtection, wincred/PCRED_PROTECTION_TYPE"
ms.topic: enum
f1_keywords: 
 - "wincred/CRED_PROTECTION_TYPE"
dev_langs:
 - c++
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - HeaderDef
api_location:
 - WinCred.h
api_name:
 - CRED_PROTECTION_TYPE
targetos: Windows
req.typenames: CRED_PROTECTION_TYPE, *PCRED_PROTECTION_TYPE
req.redist: 
ms.custom: 19H1
---

# CRED_PROTECTION_TYPE enumeration


## -description


The <b>CRED_PROTECTION_TYPE</b> enumeration specifies the security context in which credentials are encrypted when using the <a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-credprotecta">CredProtect</a> function.


## -enum-fields




### -field CredUnprotected

The credentials are not encrypted.


### -field CredUserProtection

The credentials are encrypted and can be decrypted only in the security context in which they were encrypted or in the security context of a trusted component.


### -field CredTrustedProtection

The credentials are encrypted and can only be decrypted by a trusted component.


### -field CredForSystemProtection



