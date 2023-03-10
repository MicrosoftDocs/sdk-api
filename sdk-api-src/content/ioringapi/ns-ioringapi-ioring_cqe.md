---
UID: NS:ioringapi.IORING_CQE
tech.root: fs
title: IORING_CQE
ms.date: 07/16/2021
targetos: Windows
description: Represents a completed I/O ring queue entry.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: ioringapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000 
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: IORING_CQE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ioringapi.h
api_name:
 - IORING_CQE
f1_keywords:
 - IORING_CQE
 - ioringapi/IORING_CQE
dev_langs:
 - c++
---

## -description

Represents a completed I/O ring queue entry.

## -struct-fields

### -field UserData

A **UINT_PTR** representing the user data associated with the entry. This is the same value provided as the *UserData* parameter when building the operation's submission queue entry. Applications can use this value to correlate the completion with the original operation request.

### -field ResultCode

A **HRESULT** indicating the result code of the associated I/O ring operation.

### -field Information

A **ULONG_PTR** representing information about the completed queue operation.

## -remarks

## -see-also

