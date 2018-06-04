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

# _PACKET_PROPERTY structure


## -description



Describes a packet property that is reported by the tablet driver.




## -struct-fields




### -field guid

 The property. This value is not limited to the set of predefined GUIDs. An application or a device driver may define new GUIDs at any time.


### -field PropertyMetrics

 The range, units, and resolution of the packet property.


## -see-also




<a href="https://msdn.microsoft.com/6823f2c6-2c99-4b9a-8208-041fc1f7bf82">PACKET_DESCRIPTION Structure</a>



<a href="https://msdn.microsoft.com/a6f82b69-50a2-4dfb-a0cd-c37907f5fc1c">PROPERTY_METRICS Structure</a>
 

 

