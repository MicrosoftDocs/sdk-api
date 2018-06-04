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

# PROPDESC_COLUMNINDEX_TYPE enumeration


## -description


Indicates whether or how a property can be indexed.


## -enum-fields




### -field PDCIT_NONE

Never generate any index on this property.


### -field PDCIT_ONDISK

Always build the individual value index, but build the vector index only on demand.


### -field PDCIT_INMEMORY

Obsolete.


### -field PDCIT_ONDEMAND

<b>Windows 7 and later</b>. Build the individual value index or vector index the first time the index is used in a query to filter, group, or sort. After being generated the first time, the index is maintained for future queries. Most property indexes should be built on demand, because building and maintaining indexes is expensive and they should be built only if they will be used.


### -field PDCIT_ONDISKALL

<b>Windows 7 and later</b>. Always build both the individual value index and the vector index.  


### -field PDCIT_ONDISKVECTOR

<b>Windows 7 and later</b>. Always build the vector index, but build the value index only on demand.


## -remarks



Windows Search builds indexes for the values found in the property store to efficiently support filtering, sorting, and grouping over indexed properties. There are two kinds of indexes: an individual value index that indexes an item by single values, and a vector index that indexes all the vector values of a row as a single index entry.



