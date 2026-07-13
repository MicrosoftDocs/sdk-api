---
UID: NF:ioringapi.IsIoRingOpSupported
tech.root: fs
title: IsIoRingOpSupported
ms.date: 07/16/2021
targetos: Windows
description: Queries the support of the specified operation for the specified I/O ring.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ioringapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: kernel32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000 
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-core-ioring-l1-1-2.dll
 - api-ms-win-core-ioring-l1-1-1.dll
 - api-ms-win-core-ioring-l1-1-0.dll
 - ioringapi.h
api_name:
 - IsIoRingOpSupported
f1_keywords:
 - IsIoRingOpSupported
 - ioringapi/IsIoRingOpSupported
dev_langs:
 - c++
---

## -description

Queries the support of the specified operation for the specified I/O ring.

## -parameters

### -param ioRing

An **HIORING** representing a handle to the I/O ring for which operation support is queried.

### -param op

A value from the [IORING_OP_CODE](../ntioring_x/ne-ntioring_x-ioring_op_code.md) enumeration specifying the operation for which support is queried.

## -returns

Returns an HRESULT including, but not limitted to the following:

| Value | Description |
|-------|-------------|
| S_OK  | The operation is supported. |
| S_FALSE | The operation is unsupported. |

## -remarks

Unknown operation codes are treated as unsupported. Invalid **HIORING** handles are treated as not supporting any operations. So, this method will not throw errors due to these conditions.

## -see-also

