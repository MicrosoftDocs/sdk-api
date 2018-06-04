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

# _FSCTL_QUERY_REGION_INFO_OUTPUT structure


## -description


Contains information for one or more regions.


## -struct-fields




### -field Version

The size of this structure serves as the version.  Set it to <b>sizeof</b>(<b>FSCTL_QUERY_REGION_INFO_OUTPUT</b>).


### -field Size

The size of this structure in bytes.


### -field Flags

Reserved for future use.


### -field Reserved

Reserved for future use.


### -field Alignment

Offset from the beginning of the volume to the first slab of the tiered volume. If the logical disk is made up of multiple tiers and each tier maps to a set of regions then the first tier for the volume contained on the logical disk has a certain offset within the tier that represents the offset of the volume on the logical disk.  The <b>Alignment</b> member contains this value.


### -field TotalNumberOfRegions

Total number of available regions.


### -field NumberOfRegionsReturned

Number of regions that fit in the output.


### -field Regions


<a href="https://msdn.microsoft.com/5178A987-397A-44E5-9485-221D72490124">FILE_STORAGE_TIER_REGION</a> struct that contains detailed information for each region.

