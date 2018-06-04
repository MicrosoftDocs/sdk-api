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

# _EVT_QUERY_PROPERTY_ID enumeration


## -description


Defines the identifiers that identify the query information that you can retrieve.


## -enum-fields




### -field EvtQueryNames

Identifies the property that contains the list of channel or log file names that are specified in the query. The variant type for this property is <b>EvtVarTypeString | EVT_VARIANT_TYPE_ARRAY</b>.


### -field EvtQueryStatuses

Identifies the property that contains the list of Win32 error codes that correspond directly to the list of channel or log file names that the EvtQueryNames property returns. The error codes indicate the success or failure of the query for the specific channel or log file. The variant type for this property is <b>EvtVarTypeUInt32 | EVT_VARIANT_TYPE_ARRAY</b>.


### -field EvtQueryPropertyIdEND

This enumeration value marks the end of the enumeration values.


## -see-also




<a href="https://msdn.microsoft.com/311a2060-90d9-41ec-b489-c07d3e813187">EvtGetQueryInfo</a>
 

 

