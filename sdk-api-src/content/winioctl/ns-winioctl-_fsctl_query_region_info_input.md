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

# _FSCTL_QUERY_REGION_INFO_INPUT structure


## -description


Contains the storage tier regions from the storage stack for a particular volume.


## -struct-fields




### -field Version

The size of this structure serves as the version.  Set it to <b>sizeof</b>(<b>FSCTL_QUERY_REGION_INFO_INPUT</b>).


### -field Size

The size of this structure in bytes.


### -field Flags

Reserved for future use.


### -field NumberOfTierIds

Number of entries in <b>TierIds</b>, 0 to request IDs for the entire volume.


### -field TierIds

Array of storage tiers (represented by GUID values) for which to return information.

