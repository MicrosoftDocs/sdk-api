---
UID: NS:searchapi._SEARCH_ITEM_INDEXING_STATUS
title: SEARCH_ITEM_INDEXING_STATUS (searchapi.h)
description: Describes the status of a document to be indexed.
helpviewer_keywords: ["SEARCH_ITEM_INDEXING_STATUS","SEARCH_ITEM_INDEXING_STATUS structure [search]","_search_SEARCH_ITEM_INDEXING_STATUS","search._search_SEARCH_ITEM_INDEXING_STATUS","searchapi/SEARCH_ITEM_INDEXING_STATUS"]
old-location: search\_search_SEARCH_ITEM_INDEXING_STATUS.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\search_item_indexing_status.htm
ms.date: 12/05/2018
ms.keywords: SEARCH_ITEM_INDEXING_STATUS, SEARCH_ITEM_INDEXING_STATUS structure [search], _search_SEARCH_ITEM_INDEXING_STATUS, search._search_SEARCH_ITEM_INDEXING_STATUS, searchapi/SEARCH_ITEM_INDEXING_STATUS
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
targetos: Windows
req.typenames: SEARCH_ITEM_INDEXING_STATUS
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - _SEARCH_ITEM_INDEXING_STATUS
 - searchapi/_SEARCH_ITEM_INDEXING_STATUS
 - SEARCH_ITEM_INDEXING_STATUS
 - searchapi/SEARCH_ITEM_INDEXING_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - SEARCH_ITEM_INDEXING_STATUS
---

# SEARCH_ITEM_INDEXING_STATUS structure


## -description

Describes the status of a document to be indexed.

## -struct-fields

### -field dwDocID

Type: <b>DWORD</b>

Document identifier.

### -field hrIndexingStatus

Type: <b>HRESULT</b>

An <b>HRESULT</b> value that corresponds to a system error code or a Component Object Model (COM) error code. S_OK if successful, or an error value otherwise.

