---
UID: NS:emi.EMI_CHANNEL_V2
title: EMI_CHANNEL_V2 (emi.h)
description: The EMI_CHANNEL_V2 structure provides data about an EMI V2 channel.
helpviewer_keywords: ["EMI_CHANNEL_V2","EMI_CHANNEL_V2 structure [Power Metering and Budgeting Devices]","emi/EMI_CHANNEL_V2","powermeter.emi_channel_v2"]
old-location: powermeter\emi_channel_v2.htm
tech.root: powermeter
ms.assetid: D0635128-9B95-4A53-883C-FD6CCD5B694B
ms.date: 12/05/2018
ms.keywords: EMI_CHANNEL_V2, EMI_CHANNEL_V2 structure [Power Metering and Budgeting Devices], emi/EMI_CHANNEL_V2, powermeter.emi_channel_v2
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
targetos: Windows
req.typenames: EMI_CHANNEL_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EMI_CHANNEL_V2
 - emi/EMI_CHANNEL_V2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - emi.h
api_name:
 - EMI_CHANNEL_V2
---

# EMI_CHANNEL_V2 structure


## -description

The EMI_CHANNEL_V2 structure provides data about an EMI V2 channel.

## -struct-fields

### -field MeasurementUnit

An EMI_MEASUREMENT_UNIT that specifies the unit of energy
                          measurements that can be obtained from the device from an
                          IOCTL_EMI_GET_MEASUREMENT. In EMI_VERSION_V2, the only
                          supported unit is picowatt-hours.

### -field ChannelNameSize

The size of ChannelName in bytes, including the null terminator.

### -field ChannelName

A null-terminated, Unicode string that specifies the channel name.

