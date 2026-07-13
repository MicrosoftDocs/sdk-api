---
UID: NS:ntioring_x.IORING_BUFFER_INFO
tech.root: fs
title: IORING_BUFFER_INFO
ms.date: 07/16/2021
targetos: Windows
description: Represents a data buffer that can be registered with an I/O ring.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: ntioring_x.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000 
req.target-min-winversvr: Windows Build 22000 
req.target-type: 
req.typenames: IORING_BUFFER_INFO
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ntioring_x.h
api_name:
 - IORING_BUFFER_INFO
f1_keywords:
 - IORING_BUFFER_INFO
 - ntioring_x/IORING_BUFFER_INFO
dev_langs:
 - c++
---

## -description

Represents a data buffer that can be registered with an I/O ring.

## -struct-fields

### -field Address

A **VOID** pointer representing the address of the data buffer.

### -field Length

The length of the data buffer, in bytes.

## -remarks

## -see-also

