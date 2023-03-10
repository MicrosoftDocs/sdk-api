---
UID: NE:msinkaut.TabletPropertyMetricUnit
title: TabletPropertyMetricUnit (msinkaut.h)
description: Indicates the unit of measurement of a property.
helpviewer_keywords: ["TPMU_Centimeters","TPMU_Default","TPMU_Degrees","TPMU_Grams","TPMU_Inches","TPMU_Pounds","TPMU_Radians","TPMU_Seconds","TabletPropertyMetricUnit","TabletPropertyMetricUnit enumeration [Tablet PC]","c2258c48-4062-4528-9ebb-21cdbecf70ab","msinkaut/TPMU_Centimeters","msinkaut/TPMU_Default","msinkaut/TPMU_Degrees","msinkaut/TPMU_Grams","msinkaut/TPMU_Inches","msinkaut/TPMU_Pounds","msinkaut/TPMU_Radians","msinkaut/TPMU_Seconds","msinkaut/TabletPropertyMetricUnit","tablet.tabletpropertymetricunit"]
old-location: tablet\tabletpropertymetricunit.htm
tech.root: tablet
ms.assetid: c2258c48-4062-4528-9ebb-21cdbecf70ab
ms.date: 12/05/2018
ms.keywords: TPMU_Centimeters, TPMU_Default, TPMU_Degrees, TPMU_Grams, TPMU_Inches, TPMU_Pounds, TPMU_Radians, TPMU_Seconds, TabletPropertyMetricUnit, TabletPropertyMetricUnit enumeration [Tablet PC], c2258c48-4062-4528-9ebb-21cdbecf70ab, msinkaut/TPMU_Centimeters, msinkaut/TPMU_Default, msinkaut/TPMU_Degrees, msinkaut/TPMU_Grams, msinkaut/TPMU_Inches, msinkaut/TPMU_Pounds, msinkaut/TPMU_Radians, msinkaut/TPMU_Seconds, msinkaut/TabletPropertyMetricUnit, tablet.tabletpropertymetricunit
req.header: msinkaut.h
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
req.typenames: TabletPropertyMetricUnit
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TabletPropertyMetricUnit
 - msinkaut/TabletPropertyMetricUnit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - TabletPropertyMetricUnit
---

# TabletPropertyMetricUnit enumeration


## -description

Indicates the unit of measurement of a property.

## -enum-fields

### -field TPMU_Default:0

The units are unknown.

### -field TPMU_Inches

The property value is in inches (distance units).

### -field TPMU_Centimeters

The property value is in centimeters (distance units).

### -field TPMU_Degrees

The property value is in degrees (angle units).

### -field TPMU_Radians

The property value is in radians (angle units).

### -field TPMU_Seconds

The property value is in seconds (angle units).

### -field TPMU_Pounds

The property value is in pounds (force, or mass, units).

### -field TPMU_Grams

The property value is in grams (force, or mass, units).

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpacketdescriptionpropertymetrics">GetPacketDescriptionPropertyMetrics Method [IInkStrokeDisp Interface]</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics">GetPropertyMetrics Method [IInkTablet Interface]</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>
