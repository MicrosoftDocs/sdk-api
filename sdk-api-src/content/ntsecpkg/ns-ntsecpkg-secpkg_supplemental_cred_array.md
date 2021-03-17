---
UID: NS:ntsecpkg._SECPKG_SUPPLEMENTAL_CRED_ARRAY
title: SECPKG_SUPPLEMENTAL_CRED_ARRAY (ntsecpkg.h)
description: The SECPKG_SUPPLEMENTAL_CRED_ARRAY structure contains supplemental credentials information. This structure is used by the LsaApLogonUserEx2 and UpdateCredentials functions.
helpviewer_keywords: ["*PSECPKG_SUPPLEMENTAL_CRED_ARRAY","PSECPKG_SUPPLEMENTAL_CRED_ARRAY","PSECPKG_SUPPLEMENTAL_CRED_ARRAY structure pointer [Security]","SECPKG_SUPPLEMENTAL_CRED_ARRAY","SECPKG_SUPPLEMENTAL_CRED_ARRAY structure [Security]","_ssp_secpkg_supplemental_cred_array","ntsecpkg/PSECPKG_SUPPLEMENTAL_CRED_ARRAY","ntsecpkg/SECPKG_SUPPLEMENTAL_CRED_ARRAY","security.secpkg_supplemental_cred_array"]
old-location: security\secpkg_supplemental_cred_array.htm
tech.root: security
ms.assetid: b9514e26-29a5-4ba8-a375-1723c0a1ce39
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_SUPPLEMENTAL_CRED_ARRAY, PSECPKG_SUPPLEMENTAL_CRED_ARRAY, PSECPKG_SUPPLEMENTAL_CRED_ARRAY structure pointer [Security], SECPKG_SUPPLEMENTAL_CRED_ARRAY, SECPKG_SUPPLEMENTAL_CRED_ARRAY structure [Security], _ssp_secpkg_supplemental_cred_array, ntsecpkg/PSECPKG_SUPPLEMENTAL_CRED_ARRAY, ntsecpkg/SECPKG_SUPPLEMENTAL_CRED_ARRAY, security.secpkg_supplemental_cred_array'
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
req.typenames: SECPKG_SUPPLEMENTAL_CRED_ARRAY, *PSECPKG_SUPPLEMENTAL_CRED_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_SUPPLEMENTAL_CRED_ARRAY
 - ntsecpkg/_SECPKG_SUPPLEMENTAL_CRED_ARRAY
 - PSECPKG_SUPPLEMENTAL_CRED_ARRAY
 - ntsecpkg/PSECPKG_SUPPLEMENTAL_CRED_ARRAY
 - SECPKG_SUPPLEMENTAL_CRED_ARRAY
 - ntsecpkg/SECPKG_SUPPLEMENTAL_CRED_ARRAY
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
 - SECPKG_SUPPLEMENTAL_CRED_ARRAY
---

# SECPKG_SUPPLEMENTAL_CRED_ARRAY structure


## -description

The <b>SECPKG_SUPPLEMENTAL_CRED_ARRAY</b> structure contains <a href="/windows/desktop/SecGloss/s-gly">supplemental credentials</a> information. This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_ap_logon_user_ex2">LsaApLogonUserEx2</a> and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_update_primary_credentials">UpdateCredentials</a> functions.

## -struct-fields

### -field CredentialCount

The number of supplemental credentials in the <b>Credentials</b> member.

### -field Credentials.size_is

### -field Credentials.size_is.CredentialCount

### -field Credentials

An array containing supplemental credentials.