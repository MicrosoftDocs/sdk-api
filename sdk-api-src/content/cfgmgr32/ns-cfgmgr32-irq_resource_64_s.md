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

# IRQ_Resource_64_s structure


## -description


The IRQ_RESOURCE structure is used for specifying either a resource list or a resource requirements list that describes IRQ line usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field IRQ_Header

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff548208">IRQ_DES</a> structure.


### -field IRQ_Data





#### For a resource list:

Zero.



#### For a resource requirements list:

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff548220">IRQ_RANGE</a> array.


##### - IRQ_Data.For a resource list:

Zero.


##### - IRQ_Data.For a resource requirements list:

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff548220">IRQ_RANGE</a> array.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548208">IRQ_DES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548220">IRQ_RANGE</a>
 

 

