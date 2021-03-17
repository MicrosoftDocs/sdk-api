---
UID: NS:searchapi._ITEM_INFO
title: ITEM_INFO (searchapi.h)
description: Contains information passed to the IUrlAccessor object about the current item; for example, the application name and catalog name.
helpviewer_keywords: ["ITEM_INFO","ITEM_INFO structure [search]","_search_ITEM_INFO","search._search_ITEM_INFO","searchapi/ITEM_INFO"]
old-location: search\_search_ITEM_INFO.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\item_info.htm
ms.date: 12/05/2018
ms.keywords: ITEM_INFO, ITEM_INFO structure [search], _search_ITEM_INFO, search._search_ITEM_INFO, searchapi/ITEM_INFO
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchprth.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ITEM_INFO
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - _ITEM_INFO
 - searchapi/_ITEM_INFO
 - ITEM_INFO
 - searchapi/ITEM_INFO
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
 - ITEM_INFO
---

# ITEM_INFO structure


## -description

Contains information passed to the <a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> object about the current item; for example, the application name and catalog name.

## -struct-fields

### -field dwSize

Type: <b>DWORD</b>

Size of the structure in bytes.

### -field pcwszFromEMail

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string containing an email address that is notified in case of error.

### -field pcwszApplicationName

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string containing the application name.

### -field pcwszCatalogName

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string containing the workspace name from which the crawl to this content source was initiated.

### -field pcwszContentClass

Type: <b>LPCWSTR</b>

Not used by protocol handlers.