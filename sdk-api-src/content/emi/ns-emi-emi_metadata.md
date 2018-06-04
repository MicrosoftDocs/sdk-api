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

# EMI_METADATA structure


## -description


The <b>EMI_METADATA</b> structure provides metadata about a device that supports the  Energy Metering Interface (EMI) interface, such as the hardware model and hardware revision.


## -struct-fields




### -field MeasurementUnit

An <a href="https://msdn.microsoft.com/library/windows/hardware/dn957427">EMI_MEASUREMENT_UNIT</a> that specifies the unit of energy measurements that can be obtained from the device by calling <a href="https://msdn.microsoft.com/library/windows/hardware/dn957434">IOCTL_EMI_GET_MEASUREMENT</a>. In devices that support <b>EMI_VERSION_V1</b>, the only supported unit is <b>EmiMeasurementUnitPicowattHours</b>.


### -field HardwareOEM

A null-terminated, Unicode string that contains the name of the OEM.


### -field HardwareModel

A null-terminated, Unicode string that specifies the device model.


### -field HardwareRevision

A value that specifies the current revision of the device.


### -field MeteredHardwareNameSize

The size of <b>MeteredHardwareName</b> in bytes, including the null terminator.


### -field MeteredHardwareName

A null-terminated, Unicode string that specifies the metered hardware name.


## -remarks



This structure is returned through a successful completion of an <a href="https://msdn.microsoft.com/library/windows/hardware/dn957436">IOCTL_EMI_GET_METADATA</a> IOCTL request.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn957431">Energy Metering Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn957436">IOCTL_EMI_GET_METADATA</a>
 

 

