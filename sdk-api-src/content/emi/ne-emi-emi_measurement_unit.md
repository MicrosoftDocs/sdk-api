---
UID: NE:emi.EMI_MEASUREMENT_UNIT
title: EMI_MEASUREMENT_UNIT
author: windows-sdk-content
description: The EMI_MEASUREMENT_UNIT enumeration represents the available units of energy measurements that can be retrieved from a device by using IOCTL_EMI_GET_MEASUREMENT.
old-location: powermeter\emi_measurement_unit.htm
tech.root: powermeter
ms.assetid: 02152942-A024-4D53-962A-A2ECF7E7D50C
ms.author: windowssdkdev
ms.date: 08/29/2018
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: EMI_MEASUREMENT_UNIT
req.redist: 
---

# EMI_MEASUREMENT_UNIT enumeration


## -description


The <b>EMI_MEASUREMENT_UNIT</b> enumeration represents the available units of energy measurements that can be retrieved from a device by using <a href="https://msdn.microsoft.com/E23B1ED2-A87D-419A-8BEB-136AA77258AE">IOCTL_EMI_GET_MEASUREMENT</a>. 


## -enum-fields




### -field EmiMeasurementUnitPicowattHours

The energy measurement is returned in picowatt-hours.


## -remarks



When a component calls <a href="https://msdn.microsoft.com/3A1A76B0-2A46-4C15-84BC-CE75701C30B7">IOCTL_EMI_GET_METADATA</a> to obtain the Energy Metering Interface (EMI) metadata for a device, the units of energy measurements supported by the device are returned in the <b>MeasurementUnit</b> field of the <a href="https://msdn.microsoft.com/8992AA5D-7D71-4D00-9B18-FE070D29C26E">EMI_METADATA</a> structure output parameter.

In devices that implement<b>EMI_VERSION_V1</b>, picowatt-hours is the only supported unit.




## -see-also




<a href="https://msdn.microsoft.com/8992AA5D-7D71-4D00-9B18-FE070D29C26E">EMI_METADATA</a>



<a href="https://msdn.microsoft.com/D11C97E8-8E7F-41D7-A8A9-0B5426B20818">Energy Metering Interface</a>



<a href="https://msdn.microsoft.com/E23B1ED2-A87D-419A-8BEB-136AA77258AE">IOCTL_EMI_GET_MEASUREMENT</a>
 

 

