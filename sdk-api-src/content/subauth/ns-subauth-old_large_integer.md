---
UID: NS:subauth._OLD_LARGE_INTEGER
title: OLD_LARGE_INTEGER (subauth.h)
description: Is used to represent a 64-bit signed integer value as two 32-bit integers.
helpviewer_keywords: ["*POLD_LARGE_INTEGER","OLD_LARGE_INTEGER","OLD_LARGE_INTEGER structure [Security]","POLD_LARGE_INTEGER","POLD_LARGE_INTEGER structure pointer [Security]","security.old_large_integer","subauth/OLD_LARGE_INTEGER","subauth/POLD_LARGE_INTEGER"]
old-location: security\old_large_integer.htm
tech.root: security
ms.assetid: d2becc03-10ed-4741-97a4-53f900f0e675
ms.date: 12/05/2018
ms.keywords: '*POLD_LARGE_INTEGER, OLD_LARGE_INTEGER, OLD_LARGE_INTEGER structure [Security], POLD_LARGE_INTEGER, POLD_LARGE_INTEGER structure pointer [Security], security.old_large_integer, subauth/OLD_LARGE_INTEGER, subauth/POLD_LARGE_INTEGER'
req.header: subauth.h
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
req.typenames: OLD_LARGE_INTEGER, *POLD_LARGE_INTEGER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OLD_LARGE_INTEGER
 - subauth/_OLD_LARGE_INTEGER
 - POLD_LARGE_INTEGER
 - subauth/POLD_LARGE_INTEGER
 - OLD_LARGE_INTEGER
 - subauth/OLD_LARGE_INTEGER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Subauth.h
api_name:
 - OLD_LARGE_INTEGER
---

# OLD_LARGE_INTEGER structure


## -description

The <b>OLD_LARGE_INTEGER</b> structure is used to represent a 64-bit signed integer value as two 32-bit integers.

## -struct-fields

### -field LowPart

Low-order 32 bits.

### -field HighPart

High-order 32 bits. The sign of this member determines the sign of the 64-bit integer.

