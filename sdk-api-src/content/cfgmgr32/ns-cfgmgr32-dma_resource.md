---
UID: NS:cfgmgr32.DMA_Resource_s
title: DMA_RESOURCE (cfgmgr32.h)
description: The DMA_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes DMA channel usage for a device instance.
helpviewer_keywords: ["*PDMA_RESOURCE","DMA_RESOURCE","DMA_RESOURCE structure [Device and Driver Installation]","PDMA_RESOURCE","PDMA_RESOURCE structure pointer [Device and Driver Installation]","cfgmgr32/DMA_RESOURCE","cfgmgr32/PDMA_RESOURCE","cfgmgrst_7efdb1b3-3104-4bbe-81a6-e118a75a70a3.xml","devinst.dma_resource"]
old-location: devinst\dma_resource.htm
tech.root: devinst
ms.assetid: 226a5ca1-10e1-47a7-8bd9-b153a0784ccb
ms.date: 12/05/2018
ms.keywords: '*PDMA_RESOURCE, DMA_RESOURCE, DMA_RESOURCE structure [Device and Driver Installation], PDMA_RESOURCE, PDMA_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/DMA_RESOURCE, cfgmgr32/PDMA_RESOURCE, cfgmgrst_7efdb1b3-3104-4bbe-81a6-e118a75a70a3.xml, devinst.dma_resource'
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
req.typenames: DMA_RESOURCE, *PDMA_RESOURCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DMA_Resource_s
 - cfgmgr32/DMA_Resource_s
 - PDMA_RESOURCE
 - cfgmgr32/PDMA_RESOURCE
 - DMA_RESOURCE
 - cfgmgr32/DMA_RESOURCE
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
 - DMA_RESOURCE
---

# DMA_RESOURCE structure


## -description

The DMA_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes DMA channel usage for a device instance. For more information about resource list and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field DMA_Header

A [DMA_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-dma_des) structure.

### -field DMA_Data

#### For a resource list:

Zero.



#### For a resource requirements list:

A [DMA_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-dma_range) array.

## -see-also

[DMA_DES](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-dma_des)



[DMA_RANGE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-dma_range)