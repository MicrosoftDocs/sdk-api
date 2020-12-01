---
UID: NS:tpcshrd._PROPERTY_METRICS
title: PROPERTY_METRICS (tpcshrd.h)
description: Defines the range and resolution of a packet property.
helpviewer_keywords: ["*PPROPERTY_METRICS","PPROPERTY_METRICS","PPROPERTY_METRICS structure pointer [Tablet PC]","PROPERTY_METRICS","PROPERTY_METRICS structure [Tablet PC]","a6f82b69-50a2-4dfb-a0cd-c37907f5fc1c","tablet.property_metrics","tpcshrd/PPROPERTY_METRICS","tpcshrd/PROPERTY_METRICS"]
old-location: tablet\property_metrics.htm
tech.root: tablet
ms.assetid: a6f82b69-50a2-4dfb-a0cd-c37907f5fc1c
ms.date: 12/05/2018
ms.keywords: '*PPROPERTY_METRICS, PPROPERTY_METRICS, PPROPERTY_METRICS structure pointer [Tablet PC], PROPERTY_METRICS, PROPERTY_METRICS structure [Tablet PC], a6f82b69-50a2-4dfb-a0cd-c37907f5fc1c, tablet.property_metrics, tpcshrd/PPROPERTY_METRICS, tpcshrd/PROPERTY_METRICS'
req.header: tpcshrd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: PROPERTY_METRICS, *PPROPERTY_METRICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROPERTY_METRICS
 - tpcshrd/_PROPERTY_METRICS
 - PPROPERTY_METRICS
 - tpcshrd/PPROPERTY_METRICS
 - PROPERTY_METRICS
 - tpcshrd/PROPERTY_METRICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tpcshrd.h
api_name:
 - PROPERTY_METRICS
---

# PROPERTY_METRICS structure


## -description

Defines the range and resolution of a packet  property.

## -struct-fields

### -field nLogicalMin

The minimum value, in logical units, that the tablet reports for this property. For example, a tablet reporting x-values from 0 to 9000 has a logical minimum of 0.

### -field nLogicalMax

The maximum value, in logical units, that the tablet reports for this property. For example, a tablet reporting x-values from 0 to 9000 has a logical maximum of 9000.

### -field Units

 The physical units of the property, such as inches or degrees. For a list of property units, see the <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units">PROPERTY_UNITS</a> enumeration type.

### -field fResolution

 The resolution or increment value for the <code>Units</code> member. For example, a tablet that reports 400 dots per inch (dpi) has an <i>fResoution</i> value of 400.

## -see-also

<a href="/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property">PACKET_PROPERTY Structure</a>



<a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units">PROPERTY_UNITS Enumeration</a>