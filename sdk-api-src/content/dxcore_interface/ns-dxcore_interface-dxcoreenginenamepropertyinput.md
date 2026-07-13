---
UID: NS:dxcore_interface.DXCoreEngineNamePropertyInput
title: DXCoreEngineNamePropertyInput
description: For an engine name query, represents physical adapter index, and/or engine ID, and engine name.
ms.date: 10/03/2024
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
 - DXCoreEngineNamePropertyInput
f1_keywords:
 - DXCoreEngineNamePropertyInput
 - dxcore_interface/DXCoreEngineNamePropertyInput
dev_langs:
 - c++
helpviewer_keywords:
 - DXCoreEngineNamePropertyInput
---

## -description

For an engine name query, represents physical adapter index, and/or engine ID, and engine name.

## -struct-fields

### -field adapterEngineIndex

A [DXCoreAdapterEngineIndex](./ns-dxcore_interface-dxcoreadapterengineindex.md) struct containing the physical adapter index and the engine ID.

### -field engineNameLength

The number of characters in *engineName*.

### -field engineName

The engine name string.

## -remarks

## -see-also

* [DXCoreEngineNamePropertyOutput](./ns-dxcore_interface-dxcoreenginenamepropertyoutput.md)
