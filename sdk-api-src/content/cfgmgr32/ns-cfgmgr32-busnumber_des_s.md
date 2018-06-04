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

# BusNumber_Des_s structure


## -description


The BUSNUMBER_DES structure is used for specifying either a resource list or a resource requirements list that describes bus number usage for a device instance. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547012">Hardware Resources</a>.


## -struct-fields




### -field BUSD_Count





#### For a resource list:

Zero.



#### For a resource requirements list:

The number of elements in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537831">BUSNUMBER_RANGE</a> array that is included in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537838">BUSNUMBER_RESOURCE</a> structure.


### -field BUSD_Type

Must be set to the constant value <b>BusNumberType_Range</b>.


### -field BUSD_Flags

<i>Not used.</i>


### -field BUSD_Alloc_Base





#### For a resource list:

The lowest-numbered of a range of contiguous bus numbers allocated to the device.



#### For a resource requirements list:

Zero.


### -field BUSD_Alloc_End





#### For a resource list:

The highest-numbered of a range of contiguous bus numbers allocated to the device.



#### For a resource requirements list:

Zero.


## -remarks



The BUSNUMBER_DES structure is included as a member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537838">BUSNUMBER_RESOURCE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff537831">BUSNUMBER_RANGE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537838">BUSNUMBER_RESOURCE</a>
 

 

