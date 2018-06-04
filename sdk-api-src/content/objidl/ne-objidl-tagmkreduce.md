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

# tagMKREDUCE enumeration


## -description


Specifies how far a moniker should be reduced.


## -enum-fields




### -field MKRREDUCE_ONE

Performs only one step of reducing the moniker. In general, the caller must have specific knowledge about the particular kind of moniker to take advantage of this option.


### -field MKRREDUCE_TOUSER

Reduces the moniker to a form that the user identifies as a persistent object. If no such point exists, then this option should be treated as MKRREDUCE_ALL.


### -field MKRREDUCE_THROUGHUSER

Reduces the moniker to where any further reduction would reduce it to a form that the user does not identify as a persistent object. Often, this is the same stage as MKRREDUCE_TOUSER.


### -field MKRREDUCE_ALL

Reduces the moniker until it is in its simplest form, that is, reduce it to itself.



## -see-also




<a href="https://msdn.microsoft.com/1d34da7b-e6cb-4daa-a155-45beb36e035b">IMoniker::Reduce</a>
 

 

