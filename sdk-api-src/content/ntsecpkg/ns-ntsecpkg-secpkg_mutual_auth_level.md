---
UID: NS:ntsecpkg._SECPKG_MUTUAL_AUTH_LEVEL
title: SECPKG_MUTUAL_AUTH_LEVEL (ntsecpkg.h)
description: The SECPKG_MUTUAL_AUTH_LEVEL structure contains the authentication level used by a security package.
helpviewer_keywords: ["*PSECPKG_MUTUAL_AUTH_LEVEL","PSECPKG_MUTUAL_AUTH_LEVEL","PSECPKG_MUTUAL_AUTH_LEVEL structure pointer [Security]","SECPKG_MUTUAL_AUTH_LEVEL","SECPKG_MUTUAL_AUTH_LEVEL structure [Security]","_ssp_secpkg_mutual_auth_level","ntsecpkg/PSECPKG_MUTUAL_AUTH_LEVEL","ntsecpkg/SECPKG_MUTUAL_AUTH_LEVEL","security.secpkg_mutual_auth_level"]
old-location: security\secpkg_mutual_auth_level.htm
tech.root: security
ms.assetid: f56cd322-8f82-43d7-a666-7067bf23b0a7
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_MUTUAL_AUTH_LEVEL, PSECPKG_MUTUAL_AUTH_LEVEL, PSECPKG_MUTUAL_AUTH_LEVEL structure pointer [Security], SECPKG_MUTUAL_AUTH_LEVEL, SECPKG_MUTUAL_AUTH_LEVEL structure [Security], _ssp_secpkg_mutual_auth_level, ntsecpkg/PSECPKG_MUTUAL_AUTH_LEVEL, ntsecpkg/SECPKG_MUTUAL_AUTH_LEVEL, security.secpkg_mutual_auth_level'
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
req.typenames: SECPKG_MUTUAL_AUTH_LEVEL, *PSECPKG_MUTUAL_AUTH_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_MUTUAL_AUTH_LEVEL
 - ntsecpkg/_SECPKG_MUTUAL_AUTH_LEVEL
 - PSECPKG_MUTUAL_AUTH_LEVEL
 - ntsecpkg/PSECPKG_MUTUAL_AUTH_LEVEL
 - SECPKG_MUTUAL_AUTH_LEVEL
 - ntsecpkg/SECPKG_MUTUAL_AUTH_LEVEL
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
 - SECPKG_MUTUAL_AUTH_LEVEL
---

# SECPKG_MUTUAL_AUTH_LEVEL structure


## -description

The <b>SECPKG_MUTUAL_AUTH_LEVEL</b> structure contains the authentication level used by a <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation</a> and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn">SpSetExtendedInformation</a> functions.

## -struct-fields

### -field MutualAuthLevel

The mutual authentication level.