---
UID: NE:ntsecpkg._SECPKG_NAME_TYPE
title: SECPKG_NAME_TYPE (ntsecpkg.h)
description: The SECPKG_NAME_TYPE enumeration is used to describe the type of name specified for an account.The SECPKG_NAME_TYPE enumeration is used by the GetAuthDataForUser and OpenSamUser functions.
helpviewer_keywords: ["SECPKG_NAME_TYPE","SECPKG_NAME_TYPE enumeration [Security]","SecNameAlternateId","SecNameDN","SecNameFlat","SecNameSamCompatible","_ssp_secpkg_name_type","ntsecpkg/SECPKG_NAME_TYPE","ntsecpkg/SecNameAlternateId","ntsecpkg/SecNameDN","ntsecpkg/SecNameFlat","ntsecpkg/SecNameSamCompatible","security.secpkg_name_type"]
old-location: security\secpkg_name_type.htm
tech.root: security
ms.assetid: 6a534bfa-83ec-408d-ad21-e230a7adc61e
ms.date: 12/05/2018
ms.keywords: SECPKG_NAME_TYPE, SECPKG_NAME_TYPE enumeration [Security], SecNameAlternateId, SecNameDN, SecNameFlat, SecNameSamCompatible, _ssp_secpkg_name_type, ntsecpkg/SECPKG_NAME_TYPE, ntsecpkg/SecNameAlternateId, ntsecpkg/SecNameDN, ntsecpkg/SecNameFlat, ntsecpkg/SecNameSamCompatible, security.secpkg_name_type
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
req.typenames: SECPKG_NAME_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_NAME_TYPE
 - ntsecpkg/_SECPKG_NAME_TYPE
 - SECPKG_NAME_TYPE
 - ntsecpkg/SECPKG_NAME_TYPE
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
 - SECPKG_NAME_TYPE
---

# SECPKG_NAME_TYPE enumeration


## -description

The <b>SECPKG_NAME_TYPE</b> enumeration is used to describe the type of name specified for an account.

The <b>SECPKG_NAME_TYPE</b> enumeration is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_get_auth_data_for_user">GetAuthDataForUser</a> and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_open_sam_user">OpenSamUser</a> functions.

## -enum-fields

### -field SecNameSamCompatible

The account name is compatible with the <a href="/windows/desktop/SecGloss/s-gly">Security Accounts Manager</a> (SAM). An example of a name in SAM-compatible format is <b>"</b><i>ExampleDomain</i><b>\\</b><i>UserName</i><b>"</b>.

### -field SecNameAlternateId

The account name is in the AltSecId property of the SAM account.

### -field SecNameFlat

The account name is a flat user principal name (UPN) style account name.

### -field SecNameDN

The account name is the distinguished name of the object.

### -field SecNameSPN