---
UID: NE:winsafer._SAFER_IDENTIFICATION_TYPES
title: SAFER_IDENTIFICATION_TYPES (winsafer.h)
description: Defines the possible types of identification rule structures that can be identified by the SAFER_IDENTIFICATION_HEADER structure.
helpviewer_keywords: ["SAFER_IDENTIFICATION_TYPES","SAFER_IDENTIFICATION_TYPES enumeration [Security]","SaferIdentityDefault","SaferIdentityTypeCertificate","SaferIdentityTypeImageHash","SaferIdentityTypeImageName","SaferIdentityTypeUrlZone","security.safer_identification_types","winsafer/SAFER_IDENTIFICATION_TYPES","winsafer/SaferIdentityDefault","winsafer/SaferIdentityTypeCertificate","winsafer/SaferIdentityTypeImageHash","winsafer/SaferIdentityTypeImageName","winsafer/SaferIdentityTypeUrlZone"]
old-location: security\safer_identification_types.htm
tech.root: security
ms.assetid: ced40d58-e9f1-47cc-9e05-fdaa253bb16b
ms.date: 12/05/2018
ms.keywords: SAFER_IDENTIFICATION_TYPES, SAFER_IDENTIFICATION_TYPES enumeration [Security], SaferIdentityDefault, SaferIdentityTypeCertificate, SaferIdentityTypeImageHash, SaferIdentityTypeImageName, SaferIdentityTypeUrlZone, security.safer_identification_types, winsafer/SAFER_IDENTIFICATION_TYPES, winsafer/SaferIdentityDefault, winsafer/SaferIdentityTypeCertificate, winsafer/SaferIdentityTypeImageHash, winsafer/SaferIdentityTypeImageName, winsafer/SaferIdentityTypeUrlZone
req.header: winsafer.h
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
req.typenames: SAFER_IDENTIFICATION_TYPES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SAFER_IDENTIFICATION_TYPES
 - winsafer/_SAFER_IDENTIFICATION_TYPES
 - SAFER_IDENTIFICATION_TYPES
 - winsafer/SAFER_IDENTIFICATION_TYPES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinSafer.h
api_name:
 - SAFER_IDENTIFICATION_TYPES
---

# SAFER_IDENTIFICATION_TYPES enumeration


## -description

The <b>SAFER_IDENTIFICATION_TYPES</b> enumeration type defines the possible types of identification rule structures that can be identified by the  <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_identification_header">SAFER_IDENTIFICATION_HEADER</a> structure.

## -enum-fields

### -field SaferIdentityDefault

The header is for a default level structure.

### -field SaferIdentityTypeImageName:1

The header is for a <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_pathname_identification">SAFER_PATHNAME_IDENTIFICATION</a> structure.

### -field SaferIdentityTypeImageHash

The header is for a <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_hash_identification">SAFER_HASH_IDENTIFICATION</a> structure.

### -field SaferIdentityTypeUrlZone

The header is for a <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_urlzone_identification">SAFER_URLZONE_IDENTIFICATION</a> structure.

### -field SaferIdentityTypeCertificate

The header is for a <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_pathname_identification">SAFER_PATHNAME_IDENTIFICATION</a> structure.

## -remarks

The <b>SAFER_IDENTIFICATION_TYPES</b> enumeration type is used by the <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_identification_header">SAFER_IDENTIFICATION_HEADER</a> structure.
