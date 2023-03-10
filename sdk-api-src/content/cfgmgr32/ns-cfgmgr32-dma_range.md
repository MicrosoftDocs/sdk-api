---
UID: NS:cfgmgr32.DMA_Range_s
title: DMA_RANGE (cfgmgr32.h)
description: The DMA_RANGE structure specifies a resource requirements list that describes DMA channel usage for a device instance. For more information about resource requirements lists, see Hardware Resources.
helpviewer_keywords: ["*PDMA_RANGE","DMA_RANGE","DMA_RANGE structure [Device and Driver Installation]","PDMA_RANGE","PDMA_RANGE structure pointer [Device and Driver Installation]","cfgmgr32/DMA_RANGE","cfgmgr32/PDMA_RANGE","cfgmgrst_a19d993e-d664-4218-8bae-23e97919b3a8.xml","devinst.dma_range"]
old-location: devinst\dma_range.htm
tech.root: devinst
ms.assetid: 46c80013-1863-4e02-be8d-282d2e619200
ms.date: 12/05/2018
ms.keywords: '*PDMA_RANGE, DMA_RANGE, DMA_RANGE structure [Device and Driver Installation], PDMA_RANGE, PDMA_RANGE structure pointer [Device and Driver Installation], cfgmgr32/DMA_RANGE, cfgmgr32/PDMA_RANGE, cfgmgrst_a19d993e-d664-4218-8bae-23e97919b3a8.xml, devinst.dma_range'
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DMA_RANGE, *PDMA_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DMA_Range_s
 - cfgmgr32/DMA_Range_s
 - PDMA_RANGE
 - cfgmgr32/PDMA_RANGE
 - DMA_RANGE
 - cfgmgr32/DMA_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - DMA_RANGE
---

# DMA_RANGE structure


## -description

The DMA_RANGE structure specifies a resource requirements list that describes DMA channel usage for a device instance. For more information about resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field DR_Min

The lowest-numbered DMA channel that can be allocated to the device.

### -field DR_Max

The highest-numbered DMA channel that can be allocated to the device.

### -field DR_Flags

One bit flag from [DMA_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-dma_des) structure.

## -see-also

[DMA_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-dma_des)