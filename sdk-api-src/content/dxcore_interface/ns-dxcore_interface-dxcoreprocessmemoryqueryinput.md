---
UID: NS:dxcore_interface.DXCoreProcessMemoryQueryInput
title: DXCoreProcessMemoryQueryInput
description: For a memory query, represents physical adapter index, and memory type (dedicated or shared), and process ID.
ms.date: 10/04/2024
tech.root: dxcore
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: dxcore_interface.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dxcore_interface.h
api_name:
 - DXCoreProcessMemoryQueryInput
f1_keywords:
 - DXCoreProcessMemoryQueryInput
 - dxcore_interface/DXCoreProcessMemoryQueryInput
dev_langs:
 - c++
helpviewer_keywords:
 - DXCoreProcessMemoryQueryInput
---

## -description

For a memory query, represents physical adapter index, and memory type (dedicated or shared), and process ID.

## -struct-fields

### -field physicalAdapterIndex

A physical adapter index.

### -field memoryType

A [DXCoreMemoryType](./ne-dxcore_interface-dxcorememorytype.md) struct indicating a memory type (dedicated or shared).

### -field processId

A process ID.

## -remarks

## -see-also
