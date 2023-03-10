---
UID: NS:ioringapi.IORING_HANDLE_REF
tech.root: fs
title: IORING_HANDLE_REF
ms.date: 07/16/2021
targetos: Windows
description: Represents a reference to a file handle used in an I/O ring operation.
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
req.typenames: IORING_HANDLE_REF
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ioringapi.h
api_name:
 - IORING_HANDLE_REF
f1_keywords:
 - IORING_HANDLE_REF
 - ioringapi/IORING_HANDLE_REF
dev_langs:
 - c++
---

## -description

Represents a reference to a file handle used in an I/O ring operation.

## -struct-fields

### -field Kind

A value from the [IORING_REF_KIND](ne-ioringapi-ioring_ref_kind.md) enumeration specifying the kind of handle represented by the structure.

### -field HandleUnion

### -field HandleUnion.Handle

The handle to a file if the *Kind* value is IORING_REF_RAW.

### -field HandleUnion.Index

The index of the registered file handle if the *Kind* value is IORING_REF_REGISTERED.

### -field Handle

## -remarks

## -see-also

