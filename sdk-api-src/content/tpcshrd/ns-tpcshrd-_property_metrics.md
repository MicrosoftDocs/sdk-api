---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

