---
UID: NS:ntsecpkg._SECPKG_NEGO2_INFO
title: SECPKG_NEGO2_INFO (ntsecpkg.h)
description: Contains extended package information used for NEGO2 negotiations.
helpviewer_keywords: ["*PSECPKG_NEGO2_INFO","PSECPKG_NEGO2_INFO","PSECPKG_NEGO2_INFO structure pointer [Security]","SECPKG_NEGO2_INFO","SECPKG_NEGO2_INFO structure [Security]","ntsecpkg/PSECPKG_NEGO2_INFO","ntsecpkg/SECPKG_NEGO2_INFO","security.secpkg_nego2_info"]
old-location: security\secpkg_nego2_info.htm
tech.root: security
ms.assetid: 8B093B74-DBF2-4DBD-9FDC-72FD6CC3CCA6
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_NEGO2_INFO, PSECPKG_NEGO2_INFO, PSECPKG_NEGO2_INFO structure pointer [Security], SECPKG_NEGO2_INFO, SECPKG_NEGO2_INFO structure [Security], ntsecpkg/PSECPKG_NEGO2_INFO, ntsecpkg/SECPKG_NEGO2_INFO, security.secpkg_nego2_info'
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: SECPKG_NEGO2_INFO, *PSECPKG_NEGO2_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_NEGO2_INFO
 - ntsecpkg/_SECPKG_NEGO2_INFO
 - PSECPKG_NEGO2_INFO
 - ntsecpkg/PSECPKG_NEGO2_INFO
 - SECPKG_NEGO2_INFO
 - ntsecpkg/SECPKG_NEGO2_INFO
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
 - SECPKG_NEGO2_INFO
---

# SECPKG_NEGO2_INFO structure


## -description

The <b>SECPKG_NEGO2_INFO</b> structure  contains extended package information used for NEGO2 negotiations.

This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation</a> and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn">SpSetExtendedInformation</a> functions.

## -struct-fields

### -field AuthScheme

The authentication identifier.

### -field PackageFlags

The flags associated with the authentication package.