---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IRQ_Range_s structure


## -description


The IRQ_RANGE structure specifies a resource requirements list that describes IRQ line usage for a device instance. For more information about resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field IRQR_Min

The lowest-numbered of a range of contiguous IRQ lines that can be allocated to the device.


### -field IRQR_Max

The highest-numbered of a range of contiguous IRQ lines that can be allocated to the device.


### -field IRQR_Rsvdz

 


### -field IRQR_Flags

One bit flag from <i>each</i> of the flag sets described in the table included with the description of the <b>IRQD_Flags</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548208">IRQ_DES</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548208">IRQ_DES</a>
 

 

