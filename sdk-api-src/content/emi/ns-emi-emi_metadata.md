---
UID: NS:emi.EMI_METADATA
title: EMI_METADATA
author: windows-sdk-content
description: The EMI_METADATA structure provides metadata about a device that supports the Energy Metering Interface (EMI) interface, such as the hardware model and hardware revision.
old-location: powermeter\emi_metadata.htm
old-project: powermeter
ms.assetid: 8992AA5D-7D71-4D00-9B18-FE070D29C26E
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: EMI_METADATA, EMI_METADATA structure [Power Metering and Budgeting Devices], PEMI_METADATA, PEMI_METADATA structure pointer [Power Metering and Budgeting Devices], emi/EMI_METADATA, emi/PEMI_METADATA, powermeter.emi_metadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: emi.h
req.include-header: Emi.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 10.
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
req.typenames: EMI_METADATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - emi.h
api_name:
 - EMI_METADATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

