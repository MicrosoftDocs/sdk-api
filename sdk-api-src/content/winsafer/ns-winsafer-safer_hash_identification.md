---
UID: NS:winsafer._SAFER_HASH_IDENTIFICATION
title: SAFER_HASH_IDENTIFICATION (winsafer.h)
description: Represents a hash identification rule.
helpviewer_keywords: ["*PSAFER_HASH_IDENTIFICATION","PSAFER_HASH_IDENTIFICATION","PSAFER_HASH_IDENTIFICATION structure pointer [Security]","SAFER_HASH_IDENTIFICATION","SAFER_HASH_IDENTIFICATION structure [Security]","_mnp_safer_hash_identification","security.safer_hash_identification","winsafer/PSAFER_HASH_IDENTIFICATION","winsafer/SAFER_HASH_IDENTIFICATION"]
old-location: security\safer_hash_identification.htm
tech.root: security
ms.assetid: 68b4b5f5-8220-4180-8243-b6f1fd7826bd
ms.date: 12/05/2018
ms.keywords: '*PSAFER_HASH_IDENTIFICATION, PSAFER_HASH_IDENTIFICATION, PSAFER_HASH_IDENTIFICATION structure pointer [Security], SAFER_HASH_IDENTIFICATION, SAFER_HASH_IDENTIFICATION structure [Security], _mnp_safer_hash_identification, security.safer_hash_identification, winsafer/PSAFER_HASH_IDENTIFICATION, winsafer/SAFER_HASH_IDENTIFICATION'
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
req.typenames: SAFER_HASH_IDENTIFICATION, *PSAFER_HASH_IDENTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SAFER_HASH_IDENTIFICATION
 - winsafer/_SAFER_HASH_IDENTIFICATION
 - PSAFER_HASH_IDENTIFICATION
 - winsafer/PSAFER_HASH_IDENTIFICATION
 - SAFER_HASH_IDENTIFICATION
 - winsafer/SAFER_HASH_IDENTIFICATION
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
 - SAFER_HASH_IDENTIFICATION
---

# SAFER_HASH_IDENTIFICATION structure


## -description

The <b>SAFER_HASH_IDENTIFICATION</b> structure represents a hash identification rule.

## -struct-fields

### -field header

A <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_identification_header">SAFER_IDENTIFICATION_HEADER</a> structure containing the structure header. The <b>dwIdentificationType</b> member  of the header must be <b>SaferIdentityTypeImageHash</b>, and the <b>cbStructSize</b> member  of the header must be sizeof(SAFER_HASH_IDENTIFICATION).

### -field Description

A description of the hash identification rule provided by the user.

### -field FriendlyName

A human-readable name for the hash identification rule.

### -field HashSize

The size of the <b>ImageHash</b> member in bytes. For example, if the algorithm specified by the <b>HashAlgorithm</b> member is MD5, the size is 16.

### -field ImageHash

The computed hash of the code image.

### -field HashAlgorithm

The algorithm used to compute the hash.

### -field ImageSize

The size of the original file in bytes.

### -field dwSaferFlags

Reserved for future use.