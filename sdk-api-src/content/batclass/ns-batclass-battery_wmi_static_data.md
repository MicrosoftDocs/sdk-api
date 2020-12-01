---
UID: NS:batclass._BATTERY_WMI_STATIC_DATA
title: BATTERY_WMI_STATIC_DATA (batclass.h)
description: Defines static data about a battery.
helpviewer_keywords: ["*PBATTERY_WMI_STATIC_DATA","BATTERY_WMI_STATIC_DATA","BATTERY_WMI_STATIC_DATA structure [Battery Devices]","PBATTERY_WMI_STATIC_DATA","PBATTERY_WMI_STATIC_DATA structure pointer [Battery Devices]","batclass/BATTERY_WMI_STATIC_DATA","batclass/PBATTERY_WMI_STATIC_DATA","battery.battery_wmi_static_data"]
old-location: battery\battery_wmi_static_data.htm
tech.root: battery
ms.assetid: 39930853-AB5A-4DA5-A544-7913770C4D88
ms.date: 12/05/2018
ms.keywords: '*PBATTERY_WMI_STATIC_DATA, BATTERY_WMI_STATIC_DATA, BATTERY_WMI_STATIC_DATA structure [Battery Devices], PBATTERY_WMI_STATIC_DATA, PBATTERY_WMI_STATIC_DATA structure pointer [Battery Devices], batclass/BATTERY_WMI_STATIC_DATA, batclass/PBATTERY_WMI_STATIC_DATA, battery.battery_wmi_static_data'
req.header: batclass.h
req.include-header: Batclass.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.typenames: BATTERY_WMI_STATIC_DATA, *PBATTERY_WMI_STATIC_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BATTERY_WMI_STATIC_DATA
 - batclass/_BATTERY_WMI_STATIC_DATA
 - PBATTERY_WMI_STATIC_DATA
 - batclass/PBATTERY_WMI_STATIC_DATA
 - BATTERY_WMI_STATIC_DATA
 - batclass/BATTERY_WMI_STATIC_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Batclass.h
api_name:
 - BATTERY_WMI_STATIC_DATA
---

## -description

Defines static data about a battery.

## -struct-fields

### -field Tag

A tag that identifies a specific battery.

### -field ManufactureDate

A <a href="/previous-versions/ff536284(v=vs.85)">BATTERY_MANUFACTURE_DATE</a> structure that specifies the date that the battery was manufactured.

### -field Granularity

Specifies the granularity as a <a href="/windows-hardware/drivers/ddi/content/wdm/ns-wdm-battery_reporting_scale">BATTERY_REPORTING_SCALE</a> value.

### -field Capabilities

Battery capabilities as a ULONG value encoded with one or more of the following flags:

### -field Technology

Specify zero for a primary, nonrechargeable battery, or one for a secondary, rechargeable battery.

### -field Chemistry

A four-character string indicating the type of chemistry used in the battery. Possible values include "PbAc" (Lead Acid), "LION" (Lithium Ion), "NiCd" (Nickel Cadmium), "NiMH" (Nickel Metal Hydride), "NiZn" (Nickel Zinc), and "RAM" (Rechargeable Alkaline-Manganese). Additional values might be returned as additional battery types become available.

### -field DesignedCapacity

The theoretical capacity of the battery when new, in milliwatt-hours. If BATTERY_CAPACITY_RELATIVE is set, the units are undefined.

### -field DefaultAlert1

The capacity, in milliwatt-hours, at which a low battery alert should occur.

### -field DefaultAlert2

The capacity, in milliwatt-hours, at which a warning battery alert should occur.

### -field CriticalBias

Specify the amount, in milliwatt-hours, of any small reserved charge that remains when the critical battery level shows zero. Miniclass drivers should subtract this value from the battery's <b>FullChargedCapacity</b> and remaining capacity, which is reported in <a href="/previous-versions/ff536290(v=vs.85)">BATTERY_STATUS</a>, before reporting those values.

### -field Strings

Four variable length string values are stored with the first USHORT value containing the length of the string in bytes.

## -see-also

<a href="/previous-versions/ff536284(v=vs.85)">BATTERY_MANUFACTURE_DATE</a>