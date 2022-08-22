---
UID: NS:sspi._SEC_FLAGS
tech.root: security
title: SEC_FLAGS
ms.date: 07/20/2022
targetos: Windows
description: Contains the security flags.
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
req.typenames: SEC_FLAGS, *PSEC_FLAGS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SEC_FLAGS
 - PSEC_FLAGS
 - SEC_FLAGS
f1_keywords:
 - _SEC_FLAGS
 - sspi/_SEC_FLAGS
 - PSEC_FLAGS
 - sspi/PSEC_FLAGS
 - SEC_FLAGS
 - sspi/SEC_FLAGS
dev_langs:
 - c++
helpviewer_keywords:
 - _SEC_FLAGS
---

## -description

Contains the ISC/ASC REQ flags set by the caller.

## -struct-fields

### -field Flags

The caller sets ISC/ASC REQ flags. The lower 32 bits are reserved and must be set to 0.

## -remarks

## -see-also
