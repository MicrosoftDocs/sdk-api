---
UID: NE:ntsecpkg._SECPKG_SESSIONINFO_TYPE
title: SECPKG_SESSIONINFO_TYPE (ntsecpkg.h)
description: Specifies the format of session information.
helpviewer_keywords: ["SECPKG_SESSIONINFO_TYPE","SECPKG_SESSIONINFO_TYPE enumeration [Security]","SecSessionPrimaryCred","ntsecpkg/SECPKG_SESSIONINFO_TYPE","ntsecpkg/SecSessionPrimaryCred","security.secpkg_sessioninfo_type"]
old-location: security\secpkg_sessioninfo_type.htm
tech.root: security
ms.assetid: 462b028a-9f74-4367-b89b-97fd9be301ed
ms.date: 12/05/2018
ms.keywords: SECPKG_SESSIONINFO_TYPE, SECPKG_SESSIONINFO_TYPE enumeration [Security], SecSessionPrimaryCred, ntsecpkg/SECPKG_SESSIONINFO_TYPE, ntsecpkg/SecSessionPrimaryCred, security.secpkg_sessioninfo_type
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
req.typenames: SECPKG_SESSIONINFO_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_SESSIONINFO_TYPE
 - ntsecpkg/_SECPKG_SESSIONINFO_TYPE
 - SECPKG_SESSIONINFO_TYPE
 - ntsecpkg/SECPKG_SESSIONINFO_TYPE
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
 - SECPKG_SESSIONINFO_TYPE
---

# SECPKG_SESSIONINFO_TYPE enumeration


## -description

Specifies the format of session information. This enumeration is used by the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-lsa_create_token_ex">CreateTokenEx</a> function to specify the format of the <i>SessionInformation</i> parameter.

## -enum-fields

### -field SecSessionPrimaryCred

The session information is contained in a <a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_primary_cred">SECPKG_PRIMARY_CRED</a> structure.