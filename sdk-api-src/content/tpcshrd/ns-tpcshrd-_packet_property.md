---
UID: NS:tpcshrd._PACKET_PROPERTY
title: "_PACKET_PROPERTY"
author: windows-sdk-content
description: Describes a packet property that is reported by the tablet driver.
old-location: tablet\packet_property.htm
old-project: tablet
ms.assetid: c1bd6240-7f95-421c-8622-0d7b98182d7c
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*PPACKET_PROPERTY, PACKET_PROPERTY, PACKET_PROPERTY structure [Tablet PC], PPACKET_PROPERTY, PPACKET_PROPERTY structure pointer [Tablet PC], _PACKET_PROPERTY, c1bd6240-7f95-421c-8622-0d7b98182d7c, tablet.packet_property, tpcshrd/PACKET_PROPERTY, tpcshrd/PPACKET_PROPERTY"
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
req.typenames: PACKET_PROPERTY, *PPACKET_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tpcshrd.h
api_name:
 - PACKET_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

