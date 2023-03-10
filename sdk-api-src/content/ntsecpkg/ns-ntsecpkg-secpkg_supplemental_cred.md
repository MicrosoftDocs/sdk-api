---
UID: NS:ntsecpkg._SECPKG_SUPPLEMENTAL_CRED
title: SECPKG_SUPPLEMENTAL_CRED (ntsecpkg.h)
description: The SECPKG_SUPPLEMENTAL_CRED structure contains supplemental credentials recognized by the security package.
helpviewer_keywords: ["*PSECPKG_SUPPLEMENTAL_CRED","PSECPKG_SUPPLEMENTAL_CRED","PSECPKG_SUPPLEMENTAL_CRED structure pointer [Security]","SECPKG_SUPPLEMENTAL_CRED","SECPKG_SUPPLEMENTAL_CRED structure [Security]","_ssp_secpkg_supplemental_cred","ntsecpkg/PSECPKG_SUPPLEMENTAL_CRED","ntsecpkg/SECPKG_SUPPLEMENTAL_CRED","security.secpkg_supplemental_cred"]
old-location: security\secpkg_supplemental_cred.htm
tech.root: security
ms.assetid: d5a1a986-5343-420d-8553-f1078bbd0e00
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_SUPPLEMENTAL_CRED, PSECPKG_SUPPLEMENTAL_CRED, PSECPKG_SUPPLEMENTAL_CRED structure pointer [Security], SECPKG_SUPPLEMENTAL_CRED, SECPKG_SUPPLEMENTAL_CRED structure [Security], _ssp_secpkg_supplemental_cred, ntsecpkg/PSECPKG_SUPPLEMENTAL_CRED, ntsecpkg/SECPKG_SUPPLEMENTAL_CRED, security.secpkg_supplemental_cred'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SECPKG_SUPPLEMENTAL_CRED, *PSECPKG_SUPPLEMENTAL_CRED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_SUPPLEMENTAL_CRED
 - ntsecpkg/_SECPKG_SUPPLEMENTAL_CRED
 - PSECPKG_SUPPLEMENTAL_CRED
 - ntsecpkg/PSECPKG_SUPPLEMENTAL_CRED
 - SECPKG_SUPPLEMENTAL_CRED
 - ntsecpkg/SECPKG_SUPPLEMENTAL_CRED
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
 - SECPKG_SUPPLEMENTAL_CRED
---

# SECPKG_SUPPLEMENTAL_CRED structure


## -description

The <b>SECPKG_SUPPLEMENTAL_CRED</b> structure contains <a href="/windows/desktop/SecGloss/s-gly">supplemental credentials</a> recognized by the <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

The structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spacceptcredentialsfn">SpAcceptCredentials</a> function and the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_supplemental_cred_array">SECPKG_SUPPLEMENTAL_CRED_ARRAY</a> structure.

## -struct-fields

### -field PackageName

The name of the <a href="/windows/desktop/SecGloss/a-gly">authentication package</a> that authenticated the <a href="/windows/desktop/SecGloss/c-gly">credentials</a>.

### -field CredentialSize

The size of the <b>Credentials</b> member, in bytes.

### -field Credentials

Pointer to a set of package-specific supplemental credentials.

### -field Credentials.size_is

### -field Credentials.size_is.CredentialSize