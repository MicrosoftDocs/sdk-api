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

# _EVT_EVENT_PROPERTY_ID enumeration


## -description


Defines the values that determine the query information to retrieve.


## -enum-fields




### -field EvtEventQueryIDs

Not supported. The identifier of the query that selected the event. The variant type of this property is EvtVarTypeInt32.


### -field EvtEventPath

The channel or log file from which the event came. The variant type of this property is EvtVarTypeString.


### -field EvtEventPropertyIdEND

This enumeration value marks the end of the enumeration values. It can be used to exit a loop when retrieving all the properties.


## -see-also




<a href="https://msdn.microsoft.com/69aa22a1-10c1-43bd-ae3b-d7641bed2065">EvtGetEventInfo</a>
 

 

