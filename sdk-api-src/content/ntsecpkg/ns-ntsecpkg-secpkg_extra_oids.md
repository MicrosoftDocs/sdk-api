---
UID: NS:ntsecpkg._SECPKG_EXTRA_OIDS
title: SECPKG_EXTRA_OIDS (ntsecpkg.h)
description: Contains the object identifiers (OIDs) for the extended security package.
helpviewer_keywords: ["*PSECPKG_EXTRA_OIDS","PSECPKG_EXTRA_OIDS","PSECPKG_EXTRA_OIDS structure pointer [Security]","SECPKG_EXTRA_OIDS","SECPKG_EXTRA_OIDS structure [Security]","ntsecpkg/PSECPKG_EXTRA_OIDS","ntsecpkg/SECPKG_EXTRA_OIDS","security.secpkg_extra_oids"]
old-location: security\secpkg_extra_oids.htm
tech.root: security
ms.assetid: 188EB248-F056-40F4-8A27-6BEC75F14154
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_EXTRA_OIDS, PSECPKG_EXTRA_OIDS, PSECPKG_EXTRA_OIDS structure pointer [Security], SECPKG_EXTRA_OIDS, SECPKG_EXTRA_OIDS structure [Security], ntsecpkg/PSECPKG_EXTRA_OIDS, ntsecpkg/SECPKG_EXTRA_OIDS, security.secpkg_extra_oids'
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
req.typenames: SECPKG_EXTRA_OIDS, *PSECPKG_EXTRA_OIDS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_EXTRA_OIDS
 - ntsecpkg/_SECPKG_EXTRA_OIDS
 - PSECPKG_EXTRA_OIDS
 - ntsecpkg/PSECPKG_EXTRA_OIDS
 - SECPKG_EXTRA_OIDS
 - ntsecpkg/SECPKG_EXTRA_OIDS
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
 - SECPKG_EXTRA_OIDS
---

# SECPKG_EXTRA_OIDS structure


## -description

The <b>SECPKG_EXTRA_OIDS</b> structure contains the object identifiers (OIDs) for the extended security package.

This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation</a> and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn">SpSetExtendedInformation</a> functions.

## -struct-fields

### -field OidCount

The total number of OIDs in the security package.

### -field Oids

A <a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_serialized_oid">SECPKG_SERIALIZED_OID</a> structure containing the OID data.