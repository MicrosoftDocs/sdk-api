---
UID: NS:emi.__unnamed_struct_2
title: EMI_CHANNEL_MEASUREMENT_DATA (emi.h)
description: The EMI_MEASUREMENT_DATA structure provides data about the current energy measurement and the time at which the measurement was taken.helpviewer_keywords: ["EMI_CHANNEL_MEASUREMENT_DATA","EMI_MEASUREMENT_DATA","EMI_MEASUREMENT_DATA structure [Power Metering and Budgeting Devices]","EMI_MEASUREMENT_DATA_V1","PEMI_MEASUREMENT_DATA","PEMI_MEASUREMENT_DATA structure pointer [Power Metering and Budgeting Devices]","emi/EMI_MEASUREMENT_DATA","emi/PEMI_MEASUREMENT_DATA","powermeter.emi_measurement_data"]
old-location: powermeter\emi_measurement_data.htm
tech.root: powermeter
ms.assetid: 5D8E8146-D6B4-427B-9B17-0FB4FB0372A8
ms.date: 12/05/2018
ms.keywords: EMI_CHANNEL_MEASUREMENT_DATA, EMI_MEASUREMENT_DATA, EMI_MEASUREMENT_DATA structure [Power Metering and Budgeting Devices], EMI_MEASUREMENT_DATA_V1, PEMI_MEASUREMENT_DATA, PEMI_MEASUREMENT_DATA structure pointer [Power Metering and Budgeting Devices], emi/EMI_MEASUREMENT_DATA, emi/PEMI_MEASUREMENT_DATA, powermeter.emi_measurement_data
f1_keywords:
- emi/EMI_MEASUREMENT_DATA
dev_langs:
- c++
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
targetos: Windows
req.typenames: EMI_CHANNEL_MEASUREMENT_DATA
req.redist: 
ms.custom: 19H1
---

# EMI_CHANNEL_MEASUREMENT_DATA structure


## -description


The <b>EMI_MEASUREMENT_DATA</b> structure provides data about the current energy measurement and the time at which the measurement was taken.


## -struct-fields




### -field AbsoluteEnergy

The total accumulated energy in the units specified by the [EMI_METADATA](/windows/win32/api/emi/ns-emi-emi_metadata_v1)a> struct returned by <a href="https://docs.microsoft.com/windows/desktop/api/emi/ni-emi-ioctl_emi_get_metadata">IOCTL_EMI_GET_METADATA</a>. In <b>EMI_VERSION_V1</b>, the only supported unit is picowatt-hours.


### -field AbsoluteTime

The time at which the energy measurement was taken, in 100 ns intervals. 


## -remarks



This structure is returned through a successful completion of an <a href="https://docs.microsoft.com/windows/desktop/api/emi/ni-emi-ioctl_emi_get_measurement">IOCTL_EMI_GET_MEASUREMENT</a> IOCTL request.




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/powermeter/energy-meter-interface">Energy Metering Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/emi/ni-emi-ioctl_emi_get_measurement">IOCTL_EMI_GET_MEASUREMENT</a>
 

 

