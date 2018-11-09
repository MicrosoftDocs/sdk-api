---
UID: NS:cfgmgr32.DMA_Range_s
title: DMA_Range_s
author: windows-sdk-content
description: The DMA_RANGE structure specifies a resource requirements list that describes DMA channel usage for a device instance. For more information about resource requirements lists, see Hardware Resources.
old-location: devinst\dma_range.htm
tech.root: devinst
ms.assetid: 46c80013-1863-4e02-be8d-282d2e619200
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PDMA_RANGE, DMA_RANGE, DMA_RANGE structure [Device and Driver Installation], DMA_Range_s, PDMA_RANGE, PDMA_RANGE structure pointer [Device and Driver Installation], cfgmgr32/DMA_RANGE, cfgmgr32/PDMA_RANGE, cfgmgrst_a19d993e-d664-4218-8bae-23e97919b3a8.xml, devinst.dma_range"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - DMA_RANGE
product: Windows
targetos: Windows
req.typenames: DMA_RANGE, *PDMA_RANGE
req.redist: 
---

# DMA_Range_s structure


## -description


The DMA_RANGE structure specifies a resource requirements list that describes DMA channel usage for a device instance. For more information about resource requirements lists, see <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">Hardware Resources</a>.


## -struct-fields




### -field DR_Min

The lowest-numbered DMA channel that can be allocated to the device.


### -field DR_Max

The highest-numbered DMA channel that can be allocated to the device.


### -field DR_Flags

One bit flag from <i>each</i> of the flag sets described in the table included with the description of the <b>DR_Flags</b> member of the <a href="https://msdn.microsoft.com/e357132d-ba40-4c14-813c-505aadc94a26">DMA_DES</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/e357132d-ba40-4c14-813c-505aadc94a26">DMA_DES</a>
 

 

