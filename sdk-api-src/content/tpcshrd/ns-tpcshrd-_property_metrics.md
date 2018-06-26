---
UID: NS:tpcshrd._PROPERTY_METRICS
title: "_PROPERTY_METRICS"
author: windows-sdk-content
description: Defines the range and resolution of a packet property.
old-location: tablet\property_metrics.htm
old-project: tablet
ms.assetid: a6f82b69-50a2-4dfb-a0cd-c37907f5fc1c
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: "*PPROPERTY_METRICS, PPROPERTY_METRICS, PPROPERTY_METRICS structure pointer [Tablet PC], PROPERTY_METRICS, PROPERTY_METRICS structure [Tablet PC], _PROPERTY_METRICS, a6f82b69-50a2-4dfb-a0cd-c37907f5fc1c, tablet.property_metrics, tpcshrd/PPROPERTY_METRICS, tpcshrd/PROPERTY_METRICS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: PROPERTY_METRICS, *PPROPERTY_METRICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tpcshrd.h
api_name:
 - PROPERTY_METRICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _PROPERTY_METRICS structure


## -description



Defines the range and resolution of a packet  property.




## -struct-fields




### -field nLogicalMin

The minimum value, in logical units, that the tablet reports for this property. For example, a tablet reporting x-values from 0 to 9000 has a logical minimum of 0.


### -field nLogicalMax

The maximum value, in logical units, that the tablet reports for this property. For example, a tablet reporting x-values from 0 to 9000 has a logical maximum of 9000.


### -field Units

 The physical units of the property, such as inches or degrees. For a list of property units, see the <a href="https://msdn.microsoft.com/bf207b4a-5ce2-4d2d-98ed-8020d559dca7">PROPERTY_UNITS</a> enumeration type.


### -field fResolution

 The resolution or increment value for the <code>Units</code> member. For example, a tablet that reports 400 dots per inch (dpi) has an <i>fResoution</i> value of 400.


## -see-also




<a href="https://msdn.microsoft.com/c1bd6240-7f95-421c-8622-0d7b98182d7c">PACKET_PROPERTY Structure</a>



<a href="https://msdn.microsoft.com/bf207b4a-5ce2-4d2d-98ed-8020d559dca7">PROPERTY_UNITS Enumeration</a>
 

 

