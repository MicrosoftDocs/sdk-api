---
UID: NS:dxcore_interface.DXCoreAdapterMemoryBudgetNodeSegmentGroup
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Describes a memory segment group for an adapter.
tech.root: dxcore
ms.date: 06/06/2019
ms.keywords: DXCoreAdapterMemoryBudgetNodeSegmentGroup structure, dxcore_interface.dxcoreadaptermemorybudgetnodesegmentgroup
ms.localizationpriority: low
targetos: Windows
ms.service: windows
req.assembly: 
req.construct-type: structure
req.ddi-compliance: 
req.dll: dxcore.dll
req.header: dxcore_interface.h
req.idl: 
req.include-header: dxcore.h
req.irql: 
req.kmdf-ver: 
req.lib: dxcore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 (Build 18936)
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
 - kbsyntax
api_type:
 - HeaderDef
api_location:
 - dxcore.dll
api_name:
 - DXCoreAdapterMemoryBudgetNodeSegmentGroup
---

## -description

Describes a memory segment group for an adapter.

## -struct-fields

### -field nodeIndex

Type: **uint32_t**

Specifies the device's physical adapter for which the adapter memory information is queried. For single-adapter operation, set this to zero. If there are multiple adapter nodes, then set this to the index of the node (the device's physical adapter) for which you want to query for adapter memory information (see [Multi-adapter](/windows/win32/direct3d12/multi-engine)).

### -field segmentGroup

Type: **[DXCoreSegmentGroup](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoresegmentgroup)**

Specifies the adapter memory segment grouping that you want to query about.

## -see-also

[DXCore reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters), [Multi-adapter](/windows/win32/direct3d12/multi-engine)
