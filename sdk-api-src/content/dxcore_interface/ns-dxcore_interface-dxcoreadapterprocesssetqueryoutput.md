---
UID: NS:dxcore_interface.DXCoreAdapterProcessSetQueryOutput
title: DXCoreAdapterProcessSetQueryOutput
description: Represents the number of processes (PIDs) running on the adapter.
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
 - DXCoreAdapterProcessSetQueryOutput
f1_keywords:
 - DXCoreAdapterProcessSetQueryOutput
 - dxcore_interface/DXCoreAdapterProcessSetQueryOutput
dev_langs:
 - c++
helpviewer_keywords:
 - DXCoreAdapterProcessSetQueryOutput
---

## -description

Represents the number of processes (PIDs) running on the adapter. Also see [DXCoreAdapterProcessSetQueryInput](./ns-dxcore_interface-dxcoreadapterprocesssetqueryinput.md).

## -struct-fields

### -field processesWritten

The number of PIDs actually written into the pre-allocated array in [DXCoreAdapterProcessSetQueryInput::processIds](./ns-dxcore_interface-dxcoreadapterprocesssetqueryinput.md).

### -field processesTotal

The total number of PIDs available to write.

## -remarks

## -see-also

* [DXCoreAdapterProcessSetQueryInput](./ns-dxcore_interface-dxcoreadapterprocesssetqueryinput.md)
