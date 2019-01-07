---
UID: NE:evntprov._EVENT_INFO_CLASS
title: EVENT_INFO_CLASS
author: windows-sdk-content
description: Defines a type of operation to perform on a registration object.
old-location: etw\event_info_class.htm
tech.root: ETW
ms.assetid: 76ac2b93-d5df-4504-b36d-1530bbb12ab4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EVENT_INFO_CLASS, EVENT_INFO_CLASS enumeration [ETW], EventProviderBinaryTrackInfo, EventProviderSetTraits, EventProviderUseDescriptorType, MaxEventInfo, etw.event_info_class, evntprov/EVENT_INFO_CLASS, evntprov/EventProviderBinaryTrackInfo, evntprov/EventProviderSetTraits, evntprov/EventProviderUseDescriptorType, evntprov/MaxEventInfo
ms.topic: enum
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntprov.h
api_name:
 - EVENT_INFO_CLASS
product: Windows
targetos: Windows
req.typenames: EVENT_INFO_CLASS
req.redist: 
---

# EVENT_INFO_CLASS enumeration


## -description


The <b>EVENT_INFO_CLASS</b> enumerated type defines a type of operation to perform on a registration object.


## -enum-fields




### -field EventProviderBinaryTrackInfo

Tracks the full path for the binary (DLL or EXE) from which the ETW registration was made.


### -field EventProviderSetReserved1


### -field EventProviderSetTraits

Sets traits for the provider. Implicitly indicates that the provider correctly initializes the EVENT_DATA_DESCRIPTOR values passed to EventWrite APIs, so the EVENT_DATA_DESCRIPTOR::Type field will be respected. For more information on the format of the traits, see <a href="https://msdn.microsoft.com/97755D64-BF57-4C0D-8ED4-040FC375C4AF">Provider Traits</a>.


### -field EventProviderUseDescriptorType

Indicates whether the provider correctly initializes the EVENT_DATA_DESCRIPTOR values passed to EventWrite APIs, which in turn indicates whether the EVENT_DATA_DESCRIPTOR::Type field will be respected by the EventWrite APIs. 


### -field MaxEventInfo

Maximum value for testing purposes. 


## -see-also




<a href="https://msdn.microsoft.com/e8b408ba-4bb5-4166-bf43-d18e4fe8de32">EventSetInformation</a>



<a href="https://msdn.microsoft.com/97755D64-BF57-4C0D-8ED4-040FC375C4AF">Provider Traits</a>
 

 

