---
UID: NS:cfgmgr32.DMA_Resource_s
title: DMA_Resource_s
author: windows-sdk-content
description: The DMA_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes DMA channel usage for a device instance.
old-location: devinst\dma_resource.htm
old-project: devinst
ms.assetid: 226a5ca1-10e1-47a7-8bd9-b153a0784ccb
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: "*PDMA_RESOURCE, DMA_RESOURCE, DMA_RESOURCE structure [Device and Driver Installation], DMA_Resource_s, PDMA_RESOURCE, PDMA_RESOURCE structure pointer [Device and Driver Installation], cfgmgr32/DMA_RESOURCE, cfgmgr32/PDMA_RESOURCE, cfgmgrst_7efdb1b3-3104-4bbe-81a6-e118a75a70a3.xml, devinst.dma_resource"
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
tech.root: 
req.typenames: DMA_RESOURCE, *PDMA_RESOURCE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - DMA_RESOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DMA_Resource_s structure


## -description


The DMA_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes DMA channel usage for a device instance. For more information about resource list and resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field DMA_Header

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff544758">DMA_DES</a> structure.


### -field DMA_Data





#### For a resource list:

Zero.



#### For a resource requirements list:

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff544762">DMA_RANGE</a> array.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544758">DMA_DES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544762">DMA_RANGE</a>
 

 

