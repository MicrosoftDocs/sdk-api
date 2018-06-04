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

# _SEARCH_TERM_EXPANSION enumeration


## -description


Indicates wildcard options on search terms. Used by <a href="https://msdn.microsoft.com/3af83c74-e2af-40f1-afdd-fec286b42be2">ISearchQueryHelper::get_QueryTermExpansion</a> and <a href="https://msdn.microsoft.com/edcc8a86-b677-4f84-aa6f-90ada895dbcc">ISearchQueryHelper::put_QueryTermExpansion</a> methods.


## -enum-fields




### -field SEARCH_TERM_NO_EXPANSION

No expansion is applied to search terms.


### -field SEARCH_TERM_PREFIX_ALL

All search terms are expanded.


### -field SEARCH_TERM_STEM_ALL

Stem expansion is applied to all terms.


## -remarks



While the <b>SEARCH_TERM_EXPANSION</b> enumerated type lets you specify stem expansion, Windows Search does not currently support its use with the <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a> interface.



