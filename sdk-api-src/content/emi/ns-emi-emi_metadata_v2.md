---
UID: NS:emi.EMI_METADATA_V2
title: EMI_METADATA_V2 (emi.h)
description: The EMI_METADATA_V2 structure provides metadata about a device that supports the EMI_VERSION_V2 interface. This metadata contains information about the hardware device and what EMI channels are exposed by this device.
helpviewer_keywords: ["EMI_METADATA_V2","EMI_METADATA_V2 structure [Power Metering and Budgeting Devices]","emi/EMI_METADATA_V2","powermeter.emi_metadata_v2"]
old-location: powermeter\emi_metadata_v2.htm
tech.root: powermeter
ms.assetid: E76A9253-7061-4412-81EF-D4E531331999
ms.date: 12/05/2018
ms.keywords: EMI_METADATA_V2, EMI_METADATA_V2 structure [Power Metering and Budgeting Devices], emi/EMI_METADATA_V2, powermeter.emi_metadata_v2
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
req.typenames: EMI_METADATA_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EMI_METADATA_V2
 - emi/EMI_METADATA_V2
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
 - EMI_METADATA_V2
---

# EMI_METADATA_V2 structure


## -description

The EMI_METADATA_V2 structure provides metadata about a device that supports the
EMI_VERSION_V2 interface. This metadata contains information about the hardware
device and what EMI channels are exposed by this device.

## -struct-fields

### -field HardwareOEM

A null-terminated, Unicode string that contains the name of the OEM.

### -field HardwareModel

A null-terminated, Unicode string that specifies the device model.

### -field HardwareRevision

A value that specifies the current revision of the device.

### -field ChannelCount

A value that specifies the number of EMI channels that are exposed by this device.

### -field Channels

An array of EMI_CHANNEL_V2 instances that describe the channels exposed by this device.

## -see-also

[IOCTL_EMI_GET_METADATA](ni-emi-ioctl_emi_get_metadata.md)

