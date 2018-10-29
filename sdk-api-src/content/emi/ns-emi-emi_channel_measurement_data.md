---
UID: NS:emi.EMI_CHANNEL_MEASUREMENT_DATA
title: EMI_CHANNEL_MEASUREMENT_DATA
author: windows-sdk-content
description: The EMI_CHANNEL_MEASUREMENT_DATA structure provides data about the current energy measurement and the time at which the measurement was taken for an EMI channel.
old-location: powermeter\emi_channel_measurement_data.htm
tech.root: powermeter
ms.assetid: 7485EA5D-65D2-49EB-B177-AF019EB15545
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EMI_CHANNEL_MEASUREMENT_DATA, EMI_CHANNEL_MEASUREMENT_DATA structure [Power Metering and Budgeting Devices], EMI_MEASUREMENT_DATA, EMI_MEASUREMENT_DATA_V1, emi/EMI_CHANNEL_MEASUREMENT_DATA, powermeter.emi_channel_measurement_data
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: emi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 10, version 1809.
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
 - EMI_CHANNEL_MEASUREMENT_DATA
product: Windows
targetos: Windows
req.typenames: EMI_CHANNEL_MEASUREMENT_DATA
req.redist: 
---

# EMI_CHANNEL_MEASUREMENT_DATA structure


## -description


 The EMI_CHANNEL_MEASUREMENT_DATA structure provides data about the current
        energy measurement and the time at which the measurement was taken for an
        EMI channel.


## -struct-fields




### -field AbsoluteEnergy

The total accumulated energy in units specified by the
                         MeasurementUnit field of the EMI_METADATA_V2 struct
                         returned by IOCTL_EMI_GET_METADATA. In EMI_VERSION_V2,
                         the only supported unit is picowatt-hours.


### -field AbsoluteTime

The time at which the energy measurement was taken in 100ns
                       intervals.

