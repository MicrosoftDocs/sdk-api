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

# _SEARCH_INDEXING_PHASE enumeration


## -description


Specifies the status of the current search indexing phase.


## -enum-fields




### -field SEARCH_INDEXING_PHASE_GATHERER

Sent in the event that an error occurs while a notification is in the gatherer. For instance, if the notification fails the exclusion-rule tests, a status update will be sent with the error.


### -field SEARCH_INDEXING_PHASE_QUERYABLE

The document will be returned in queries. It is currently only in the volatile indexes.


### -field SEARCH_INDEXING_PHASE_PERSISTED

The document has moved from the volatile index to the persisted-file-based index.

