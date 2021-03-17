---
UID: NS:ntsecpkg._SECPKG_SERIALIZED_OID
title: SECPKG_SERIALIZED_OID (ntsecpkg.h)
description: Contains the security package's object identifier (OID).
helpviewer_keywords: ["*PSECPKG_SERIALIZED_OID","PSECPKG_SERIALIZED_OID","PSECPKG_SERIALIZED_OID structure pointer [Security]","SECPKG_SERIALIZED_OID","SECPKG_SERIALIZED_OID structure [Security]","ntsecpkg/PSECPKG_SERIALIZED_OID","ntsecpkg/SECPKG_SERIALIZED_OID","security.secpkg_serialized_oid"]
old-location: security\secpkg_serialized_oid.htm
tech.root: security
ms.assetid: 54CF931B-AD1F-4370-A2AF-5DF4BC9EA007
ms.date: 12/05/2018
ms.keywords: '*PSECPKG_SERIALIZED_OID, PSECPKG_SERIALIZED_OID, PSECPKG_SERIALIZED_OID structure pointer [Security], SECPKG_SERIALIZED_OID, SECPKG_SERIALIZED_OID structure [Security], ntsecpkg/PSECPKG_SERIALIZED_OID, ntsecpkg/SECPKG_SERIALIZED_OID, security.secpkg_serialized_oid'
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
req.typenames: SECPKG_SERIALIZED_OID, *PSECPKG_SERIALIZED_OID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECPKG_SERIALIZED_OID
 - ntsecpkg/_SECPKG_SERIALIZED_OID
 - PSECPKG_SERIALIZED_OID
 - ntsecpkg/PSECPKG_SERIALIZED_OID
 - SECPKG_SERIALIZED_OID
 - ntsecpkg/SECPKG_SERIALIZED_OID
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
 - SECPKG_SERIALIZED_OID
---

# SECPKG_SERIALIZED_OID structure


## -description

The <b>SECPKG_SERIALIZED_OID</b> structure contains the security package's object identifier (OID). 

This structure is used by the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spgetextendedinformationfn">SpGetExtendedInformation</a> and 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spsetextendedinformationfn">SpSetExtendedInformation</a> functions.

## -struct-fields

### -field OidLength

The length of the OID.

### -field OidAttributes

The attributes of the OID.

### -field OidValue

The value of the OID. The value of SECPKG_MAX_OID_LENGTH is currently set to 32.