---
UID: NS:emi.EMI_MEASUREMENT_DATA
title: EMI_MEASUREMENT_DATA
author: windows-sdk-content
description: The EMI_MEASUREMENT_DATA structure provides data about the current energy measurement and the time at which the measurement was taken.
old-location: powermeter\emi_measurement_data.htm
old-project: powermeter
ms.assetid: 5D8E8146-D6B4-427B-9B17-0FB4FB0372A8
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: EMI_MEASUREMENT_DATA, EMI_MEASUREMENT_DATA structure [Power Metering and Budgeting Devices], PEMI_MEASUREMENT_DATA, PEMI_MEASUREMENT_DATA structure pointer [Power Metering and Budgeting Devices], emi/EMI_MEASUREMENT_DATA, emi/PEMI_MEASUREMENT_DATA, powermeter.emi_measurement_data
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
req.typenames: EMI_MEASUREMENT_DATA
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

