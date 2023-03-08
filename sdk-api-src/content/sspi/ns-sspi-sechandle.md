---
UID: NS:sspi._SecHandle
tech.root: security
title: SecHandle
ms.date: 07/20/2022
targetos: Windows
description: Represents a security handle.
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
req.typenames: SecHandle, *PSecHandle
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SecHandle
 - PSecHandle
 - SecHandle
f1_keywords:
 - _SecHandle
 - sspi/_SecHandle
 - PSecHandle
 - sspi/PSecHandle
 - SecHandle
 - sspi/SecHandle
dev_langs:
 - c++
helpviewer_keywords:
 - _SecHandle
---

## -description

Represents a security handle.

## -struct-fields

### -field dwLower

The lower 32 bits of the handle.

### -field dwUpper

The upper 32 bits of the handle.

## -remarks

## -see-also
