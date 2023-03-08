---
UID: NE:emi.EMI_MEASUREMENT_UNIT
title: EMI_MEASUREMENT_UNIT (emi.h)
description: The EMI_MEASUREMENT_UNIT enumeration represents the available units of energy measurements that can be retrieved from a device by using IOCTL_EMI_GET_MEASUREMENT.
helpviewer_keywords: ["EMI_MEASUREMENT_UNIT","EMI_MEASUREMENT_UNIT enumeration [Power Metering and Budgeting Devices]","EmiMeasurementUnitPicowattHours","emi/EMI_MEASUREMENT_UNIT","emi/EmiMeasurementUnitPicowattHours","powermeter.emi_measurement_unit"]
old-location: powermeter\emi_measurement_unit.htm
tech.root: powermeter
ms.assetid: 02152942-A024-4D53-962A-A2ECF7E7D50C
ms.date: 12/05/2018
ms.keywords: EMI_MEASUREMENT_UNIT, EMI_MEASUREMENT_UNIT enumeration [Power Metering and Budgeting Devices], EmiMeasurementUnitPicowattHours, emi/EMI_MEASUREMENT_UNIT, emi/EmiMeasurementUnitPicowattHours, powermeter.emi_measurement_unit
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
req.typenames: EMI_MEASUREMENT_UNIT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EMI_MEASUREMENT_UNIT
 - emi/EMI_MEASUREMENT_UNIT
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
 - EMI_MEASUREMENT_UNIT
---

# EMI_MEASUREMENT_UNIT enumeration


## -description

The <b>EMI_MEASUREMENT_UNIT</b> enumeration represents the available units of energy measurements that can be retrieved from a device by using <a href="/windows/desktop/api/emi/ni-emi-ioctl_emi_get_measurement">IOCTL_EMI_GET_MEASUREMENT</a>.

## -enum-fields

### -field EmiMeasurementUnitPicowattHours

The energy measurement is returned in picowatt-hours.

## -remarks

When a component calls [EMI_METADATA](./ns-emi-emi_metadata_v1.md) structure output parameter.

In devices that implement <b>EMI_VERSION_V1</b>, picowatt-hours is the only supported unit.

## -see-also

[EMI_METADATA](./ns-emi-emi_metadata_v1.md)



<a href="/windows-hardware/drivers/powermeter/energy-meter-interface">Energy Metering Interface</a>



<a href="/windows/desktop/api/emi/ni-emi-ioctl_emi_get_measurement">IOCTL_EMI_GET_MEASUREMENT</a>

