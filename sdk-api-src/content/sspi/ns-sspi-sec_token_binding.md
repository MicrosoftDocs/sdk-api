---
UID: NS:sspi._SEC_TOKEN_BINDING
tech.root: security
title: SEC_TOKEN_BINDING
ms.date: 07/20/2022
targetos: Windows
description: Stores the token binding information.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: SEC_TOKEN_BINDING, *PSEC_TOKEN_BINDING
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SEC_TOKEN_BINDING
 - PSEC_TOKEN_BINDING
 - SEC_TOKEN_BINDING
f1_keywords:
 - _SEC_TOKEN_BINDING
 - sspi/_SEC_TOKEN_BINDING
 - PSEC_TOKEN_BINDING
 - sspi/PSEC_TOKEN_BINDING
 - SEC_TOKEN_BINDING
 - sspi/SEC_TOKEN_BINDING
dev_langs:
 - c++
helpviewer_keywords:
 - _SEC_TOKEN_BINDING
---

## -description

Contains Token Binding version information and parameter IDs.

## -struct-fields

### -field MajorVersion

The supported major version of the Token Binding protocol.

### -field MinorVersion

The supported minor version of the Token Binding protocol.

### -field KeyParametersSize

The size (in bytes) of the Token Binding key parameter IDs array.

### -field KeyParameters

The Token Binding key parameter IDs, most preferred first.

## -remarks

## -see-also
