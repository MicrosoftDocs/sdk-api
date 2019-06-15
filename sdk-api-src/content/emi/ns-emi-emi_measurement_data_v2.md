---
UID: NS:emi.__unnamed_struct_6
title: EMI_MEASUREMENT_DATA_V2 (emi.h)
author: windows-sdk-content
description: The EMI_MEASUREMENT_DATA_V2 structure provides data about the current energy measurement data for all channels of an EMI_VERSION_V2 device.
old-location: powermeter\emi_measurement_data_v2.htm
tech.root: powermeter
ms.assetid: 18715936-7401-4F32-AD80-8AE5575AECA7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EMI_MEASUREMENT_DATA_V2, EMI_MEASUREMENT_DATA_V2 structure [Power Metering and Budgeting Devices], emi/EMI_MEASUREMENT_DATA_V2, powermeter.emi_measurement_data_v2
ms.topic: struct
f1_keywords: ["emi/EMI_MEASUREMENT_DATA_V2"]
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
 - EMI_MEASUREMENT_DATA_V2
product: Windows
targetos: Windows
req.typenames: EMI_MEASUREMENT_DATA_V2
req.redist: 
ms.custom: 19H1
---

# EMI_MEASUREMENT_DATA_V2 structure


## -description


The EMI_MEASUREMENT_DATA_V2 structure provides data about the current energy
        measurement data for all channels of an EMI_VERSION_V2 device. Each index in
        ChannelData must correspond to the measurement of the channel defined at the
        same index in Channels field of the EMI_METADATA_V2 struct.


## -struct-fields




### -field ChannelData

The channel measurement for each channel exposed by this device.

