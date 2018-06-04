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

# _EVENT_INFO_CLASS enumeration


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
 

 

