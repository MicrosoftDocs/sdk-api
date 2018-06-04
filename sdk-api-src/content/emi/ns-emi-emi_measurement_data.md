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

# EMI_MEASUREMENT_DATA structure


## -description


The <b>EMI_MEASUREMENT_DATA</b> structure provides data about the current energy measurement and the time at which the measurement was taken.


## -struct-fields




### -field AbsoluteEnergy

The total accumulated energy in the units specified by the <b>MeasurementUnit</b> field of the 	<a href="https://msdn.microsoft.com/library/windows/hardware/dn957428">EMI_METADATA</a> struct returned by <a href="https://msdn.microsoft.com/library/windows/hardware/dn957436">IOCTL_EMI_GET_METADATA</a>. In <b>EMI_VERSION_V1</b>, the only supported unit is picowatt-hours.


### -field AbsoluteTime

The time at which the energy measurement was taken, in 100 ns intervals. 


## -remarks



This structure is returned through a successful completion of an <a href="https://msdn.microsoft.com/library/windows/hardware/dn957434">IOCTL_EMI_GET_MEASUREMENT</a> IOCTL request.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn957431">Energy Metering Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn957434">IOCTL_EMI_GET_MEASUREMENT</a>
 

 

