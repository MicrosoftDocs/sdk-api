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

# PROPDESC_SEARCHINFO_FLAGS enumeration


## -description


Determines whether and how a property is indexed by Windows Search.


## -enum-fields




### -field PDSIF_DEFAULT

The property is not indexed.


### -field PDSIF_ININVERTEDINDEX

The property is in an inverted index to help speed searches.


### -field PDSIF_ISCOLUMN

The property is indexed by Windows Search.


### -field PDSIF_ISCOLUMNSPARSE

The property is indexed to save space for properties that are not present on all files.


### -field PDSIF_ALWAYSINCLUDE

<b>Windows 7 and later</b>. The property mnemonics are recognized by AQS even if the property is not a column (PDSIF_ISCOLUMN).


### -field PDSIF_USEFORTYPEAHEAD

Check this property for matches when looking for type ahead results.  


## -remarks



For third parties, the PDSIF_ALWAYSINCLUDE flag can be referred to in user-specified query strings, even though its value may not be retrievable from the index in query results. The meaning of the PDSIF_ALWAYSINCLUDE flag to the indexer when a third party sets the flag through a custom schema definition is that it enables users to refer to this property in query strings even though its value is not stored in the index.

Property mnemonics refers to a shortened name for a property. 



