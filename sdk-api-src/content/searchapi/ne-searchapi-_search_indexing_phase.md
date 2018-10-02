---
UID: NE:searchapi._SEARCH_INDEXING_PHASE
title: "_SEARCH_INDEXING_PHASE"
author: windows-sdk-content
description: Specifies the status of the current search indexing phase.
old-location: search\_search_SEARCH_INDEXING_PHASE.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\search_indexing_phase.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: SEARCH_INDEXING_PHASE, SEARCH_INDEXING_PHASE enumeration [search], SEARCH_INDEXING_PHASE_GATHERER, SEARCH_INDEXING_PHASE_PERSISTED, SEARCH_INDEXING_PHASE_QUERYABLE, _SEARCH_INDEXING_PHASE, _search_SEARCH_INDEXING_PHASE, search._search_SEARCH_INDEXING_PHASE, searchapi/SEARCH_INDEXING_PHASE, searchapi/SEARCH_INDEXING_PHASE_GATHERER, searchapi/SEARCH_INDEXING_PHASE_PERSISTED, searchapi/SEARCH_INDEXING_PHASE_QUERYABLE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchntfyinlinesite.idl
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
 - Searchapi.h
api_name:
 - SEARCH_INDEXING_PHASE
product: Windows
targetos: Windows
req.typenames: SEARCH_INDEXING_PHASE
req.redist: Windows Desktop Search (WDS) 3.0
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

