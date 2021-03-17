---
UID: NS:ntsecpkg._ENCRYPTED_CREDENTIALW
title: ENCRYPTED_CREDENTIALW (ntsecpkg.h)
description: Represents an encrypted credential.
helpviewer_keywords: ["*PENCRYPTED_CREDENTIALW","ENCRYPTED_CREDENTIALW","ENCRYPTED_CREDENTIALW structure [Security]","PENCRYPTED_CREDENTIALW","PENCRYPTED_CREDENTIALW structure pointer [Security]","ntsecpkg/ENCRYPTED_CREDENTIALW","ntsecpkg/PENCRYPTED_CREDENTIALW","security.encrypted_credentialw"]
old-location: security\encrypted_credentialw.htm
tech.root: security
ms.assetid: b350ef3d-5ed5-4355-ae3a-f03fafff2f52
ms.date: 12/05/2018
ms.keywords: '*PENCRYPTED_CREDENTIALW, ENCRYPTED_CREDENTIALW, ENCRYPTED_CREDENTIALW structure [Security], PENCRYPTED_CREDENTIALW, PENCRYPTED_CREDENTIALW structure pointer [Security], ntsecpkg/ENCRYPTED_CREDENTIALW, ntsecpkg/PENCRYPTED_CREDENTIALW, security.encrypted_credentialw'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ENCRYPTED_CREDENTIALW, *PENCRYPTED_CREDENTIALW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENCRYPTED_CREDENTIALW
 - ntsecpkg/_ENCRYPTED_CREDENTIALW
 - PENCRYPTED_CREDENTIALW
 - ntsecpkg/PENCRYPTED_CREDENTIALW
 - ENCRYPTED_CREDENTIALW
 - ntsecpkg/ENCRYPTED_CREDENTIALW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - ENCRYPTED_CREDENTIALW
---

# ENCRYPTED_CREDENTIALW structure


## -description

Represents an encrypted credential.

## -struct-fields

### -field Cred

A pointer to a <a href="/windows/desktop/api/wincred/ns-wincred-credentiala">CREDENTIAL</a> structure that contains the encrypted credential.

### -field ClearCredentialBlobSize

The size, in bytes, of the unencrypted credential.

## -see-also

<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-credfreecredentialsfn">CrediFreeCredentials</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-credreadfn">CrediRead</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-credreaddomaincredentialsfn">CrediReadDomainCredentials</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-credwritefn">CrediWrite</a>



<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>