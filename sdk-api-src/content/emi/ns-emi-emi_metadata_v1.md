---
UID: NS:emi.EMI_METADATA_V1
title: EMI_METADATA_V1 (emi.h)
description: The EMI_METADATA structure provides metadata about a device that supports the Energy Metering Interface (EMI) interface, such as the hardware model and hardware revision.
helpviewer_keywords: ["EMI_METADATA","EMI_METADATA structure [Power Metering and Budgeting Devices]","EMI_METADATA_V1","PEMI_METADATA","PEMI_METADATA structure pointer [Power Metering and Budgeting Devices]","emi/EMI_METADATA","emi/PEMI_METADATA","powermeter.emi_metadata"]
old-location: powermeter\emi_metadata.htm
tech.root: powermeter
ms.assetid: 8992AA5D-7D71-4D00-9B18-FE070D29C26E
ms.date: 12/05/2018
ms.keywords: EMI_METADATA, EMI_METADATA structure [Power Metering and Budgeting Devices], EMI_METADATA_V1, PEMI_METADATA, PEMI_METADATA structure pointer [Power Metering and Budgeting Devices], emi/EMI_METADATA, emi/PEMI_METADATA, powermeter.emi_metadata
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
targetos: Windows
req.typenames: EMI_METADATA_V1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EMI_METADATA_V1
 - emi/EMI_METADATA_V1
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
 - EMI_METADATA
---

# EMI_METADATA_V1 structure


## -description

The <b>EMI_METADATA</b> structure provides metadata about a device that supports the  Energy Metering Interface (EMI) interface, such as the hardware model and hardware revision.

## -struct-fields

### -field MeasurementUnit

An <a href="/windows/desktop/api/emi/ne-emi-emi_measurement_unit">EMI_MEASUREMENT_UNIT</a> that specifies the unit of energy measurements that can be obtained from the device by calling <a href="/windows/desktop/api/emi/ni-emi-ioctl_emi_get_measurement">IOCTL_EMI_GET_MEASUREMENT</a>. In devices that support <b>EMI_VERSION_V1</b>, the only supported unit is <b>EmiMeasurementUnitPicowattHours</b>.

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

This structure is returned through a successful completion of an <a href="/windows/desktop/api/emi/ni-emi-ioctl_emi_get_metadata">IOCTL_EMI_GET_METADATA</a> IOCTL request.

## -see-also

<a href="/windows-hardware/drivers/powermeter/energy-meter-interface">Energy Metering Interface</a>

<a href="/windows/desktop/api/emi/ni-emi-ioctl_emi_get_metadata">IOCTL_EMI_GET_METADATA</a>

