---
UID: NE:emi.EMI_MEASUREMENT_UNIT
title: EMI_MEASUREMENT_UNIT
author: windows-sdk-content
description: The EMI_MEASUREMENT_UNIT enumeration represents the available units of energy measurements that can be retrieved from a device by using IOCTL_EMI_GET_MEASUREMENT.
old-location: powermeter\emi_measurement_unit.htm
old-project: powermeter
ms.assetid: 02152942-A024-4D53-962A-A2ECF7E7D50C
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: EMI_MEASUREMENT_UNIT, EMI_MEASUREMENT_UNIT enumeration [Power Metering and Budgeting Devices], EmiMeasurementUnitPicowattHours, emi/EMI_MEASUREMENT_UNIT, emi/EmiMeasurementUnitPicowattHours, powermeter.emi_measurement_unit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: EMI_MEASUREMENT_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - emi.h
api_name:
 - EMI_MEASUREMENT_UNIT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

