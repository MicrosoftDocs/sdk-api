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

# EMI_MEASUREMENT_UNIT enumeration


## -description


The <b>EMI_MEASUREMENT_UNIT</b> enumeration represents the available units of energy measurements that can be retrieved from a device by using <a href="https://msdn.microsoft.com/library/windows/hardware/dn957434">IOCTL_EMI_GET_MEASUREMENT</a>. 


## -enum-fields




### -field EmiMeasurementUnitPicowattHours

The energy measurement is returned in picowatt-hours.


## -remarks



When a component calls <a href="https://msdn.microsoft.com/library/windows/hardware/dn957436">IOCTL_EMI_GET_METADATA</a> to obtain the Energy Metering Interface (EMI) metadata for a device, the units of energy measurements supported by the device are returned in the <b>MeasurementUnit</b> field of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn957428">EMI_METADATA</a> structure output parameter.

In devices that implement<b>EMI_VERSION_V1</b>, picowatt-hours is the only supported unit.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn957428">EMI_METADATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn957431">Energy Metering Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn957434">IOCTL_EMI_GET_MEASUREMENT</a>
 

 

