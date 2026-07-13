---
UID: NS:dxcore_interface.DXCoreAdapterProcessSetQueryInput
title: DXCoreAdapterProcessSetQueryInput
description: Represents an array of processes (PIDs) running on the adapter.
ms.date: 10/02/2024
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
 - DXCoreAdapterProcessSetQueryInput
f1_keywords:
 - DXCoreAdapterProcessSetQueryInput
 - dxcore_interface/DXCoreAdapterProcessSetQueryInput
dev_langs:
 - c++
helpviewer_keywords:
 - DXCoreAdapterProcessSetQueryInput
---

## -description

Represents an array of processes (PIDs) running on the adapter. Also see [DXCoreAdapterProcessSetQueryOutput](./ns-dxcore_interface-dxcoreadapterprocesssetqueryoutput.md).

## -struct-fields

### -field arraySize

The number of elements in *processIds*.

### -field processIds

An array which, on return, contains the IDs of the processes running on the adapter.

## -remarks

## -see-also

* [DXCoreAdapterProcessSetQueryOutput](./ns-dxcore_interface-dxcoreadapterprocesssetqueryoutput.md)
