---
UID: NS:emi.__unnamed_struct_2
title: EMI_CHANNEL_MEASUREMENT_DATA
author: windows-sdk-content
description: The EMI_MEASUREMENT_DATA structure provides data about the current energy measurement and the time at which the measurement was taken.
old-location: powermeter\emi_measurement_data.htm
tech.root: powermeter
ms.assetid: 5D8E8146-D6B4-427B-9B17-0FB4FB0372A8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EMI_CHANNEL_MEASUREMENT_DATA, EMI_MEASUREMENT_DATA, EMI_MEASUREMENT_DATA structure [Power Metering and Budgeting Devices], EMI_MEASUREMENT_DATA_V1, PEMI_MEASUREMENT_DATA, PEMI_MEASUREMENT_DATA structure pointer [Power Metering and Budgeting Devices], emi/EMI_MEASUREMENT_DATA, emi/PEMI_MEASUREMENT_DATA, powermeter.emi_measurement_data
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - EMI_MEASUREMENT_DATA
product: Windows
targetos: Windows
req.typenames: EMI_CHANNEL_MEASUREMENT_DATA
req.redist: 
---

# EMI_CHANNEL_MEASUREMENT_DATA structure


## -description


The <b>EMI_MEASUREMENT_DATA</b> structure provides data about the current energy measurement and the time at which the measurement was taken.


## -struct-fields




### -field AbsoluteEnergy

The total accumulated energy in the units specified by the <b>MeasurementUnit</b> field of the 	<a href="https://msdn.microsoft.com/8992AA5D-7D71-4D00-9B18-FE070D29C26E">EMI_METADATA</a> struct returned by <a href="https://msdn.microsoft.com/3A1A76B0-2A46-4C15-84BC-CE75701C30B7">IOCTL_EMI_GET_METADATA</a>. In <b>EMI_VERSION_V1</b>, the only supported unit is picowatt-hours.


### -field AbsoluteTime

The time at which the energy measurement was taken, in 100 ns intervals. 


## -remarks



This structure is returned through a successful completion of an <a href="https://msdn.microsoft.com/E23B1ED2-A87D-419A-8BEB-136AA77258AE">IOCTL_EMI_GET_MEASUREMENT</a> IOCTL request.




## -see-also




<a href="https://msdn.microsoft.com/D11C97E8-8E7F-41D7-A8A9-0B5426B20818">Energy Metering Interface</a>



<a href="https://msdn.microsoft.com/E23B1ED2-A87D-419A-8BEB-136AA77258AE">IOCTL_EMI_GET_MEASUREMENT</a>
 

 

