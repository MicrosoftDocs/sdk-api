---
UID: NS:cfgmgr32.IRQ_Range_s
title: IRQ_Range_s
author: windows-sdk-content
description: The IRQ_RANGE structure specifies a resource requirements list that describes IRQ line usage for a device instance. For more information about resource requirements lists, see Hardware Resources.
old-location: devinst\irq_range.htm
tech.root: devinst
ms.assetid: 973834cc-0798-414f-a937-5ab14c214559
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PIRQ_RANGE, IRQ_RANGE, IRQ_RANGE structure [Device and Driver Installation], IRQ_Range_s, PIRQ_RANGE, PIRQ_RANGE structure pointer [Device and Driver Installation], cfgmgr32/IRQ_RANGE, cfgmgr32/PIRQ_RANGE, cfgmgrst_6ee86ca7-d07d-4f1b-9c94-96766a5fd4cb.xml, devinst.irq_range"
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
 - IRQ_RANGE
product: Windows
targetos: Windows
req.typenames: IRQ_RANGE, *PIRQ_RANGE
req.redist: 
---

# IRQ_Range_s structure


## -description


The IRQ_RANGE structure specifies a resource requirements list that describes IRQ line usage for a device instance. For more information about resource requirements lists, see <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">Hardware Resources</a>.


## -struct-fields




### -field IRQR_Min

The lowest-numbered of a range of contiguous IRQ lines that can be allocated to the device.


### -field IRQR_Max

The highest-numbered of a range of contiguous IRQ lines that can be allocated to the device.


### -field IRQR_Rsvdz

 


### -field IRQR_Flags

One bit flag from <i>each</i> of the flag sets described in the table included with the description of the <b>IRQD_Flags</b> member of the <a href="https://msdn.microsoft.com/fa8b8d96-6642-4f5a-b65c-0c7470340251">IRQ_DES</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/fa8b8d96-6642-4f5a-b65c-0c7470340251">IRQ_DES</a>
 

 

