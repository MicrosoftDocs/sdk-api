---
UID: NS:searchapi._SEARCH_ITEM_INDEXING_STATUS
title: "_SEARCH_ITEM_INDEXING_STATUS"
author: windows-driver-content
description: Describes the status of a document to be indexed.
old-location: search\_search_SEARCH_ITEM_INDEXING_STATUS.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\search_item_indexing_status.htm
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: SEARCH_ITEM_INDEXING_STATUS, SEARCH_ITEM_INDEXING_STATUS structure [search], _SEARCH_ITEM_INDEXING_STATUS, _search_SEARCH_ITEM_INDEXING_STATUS, search._search_SEARCH_ITEM_INDEXING_STATUS, searchapi/SEARCH_ITEM_INDEXING_STATUS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: SEARCH_ITEM_INDEXING_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Searchapi.h
api_name:
-	SEARCH_ITEM_INDEXING_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _SEARCH_ITEM_INDEXING_STATUS structure


## -description


Describes the status of a document to be indexed.


## -struct-fields




### -field dwDocID

Type: <b>DWORD</b>

Document identifier.


### -field hrIndexingStatus

Type: <b>HRESULT</b>

An <b>HRESULT</b> value that corresponds to a system error code or a Component Object Model (COM) error code. S_OK if successful, or an error value otherwise.

