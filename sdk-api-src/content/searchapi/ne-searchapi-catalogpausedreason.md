---
UID: NE:searchapi._CatalogPausedReason
title: CatalogPausedReason (searchapi.h)
description: Used by ISearchCatalogManager::GetCatalogStatus to determine the reason the catalog is paused.
helpviewer_keywords: ["CATALOG_PAUSED_REASON_DELAYED_RECOVERY","CATALOG_PAUSED_REASON_EXTERNAL","CATALOG_PAUSED_REASON_HIGH_CPU","CATALOG_PAUSED_REASON_HIGH_IO","CATALOG_PAUSED_REASON_HIGH_NTF_RATE","CATALOG_PAUSED_REASON_LOW_BATTERY","CATALOG_PAUSED_REASON_LOW_DISK","CATALOG_PAUSED_REASON_LOW_MEMORY","CATALOG_PAUSED_REASON_NONE","CATALOG_PAUSED_REASON_UPGRADING","CATALOG_PAUSED_REASON_USER_ACTIVE","CatalogPausedReason","CatalogPausedReason enumeration [search]","_search_CatalogPausedReason","search._search_CatalogPausedReason","searchapi/CATALOG_PAUSED_REASON_DELAYED_RECOVERY","searchapi/CATALOG_PAUSED_REASON_EXTERNAL","searchapi/CATALOG_PAUSED_REASON_HIGH_CPU","searchapi/CATALOG_PAUSED_REASON_HIGH_IO","searchapi/CATALOG_PAUSED_REASON_HIGH_NTF_RATE","searchapi/CATALOG_PAUSED_REASON_LOW_BATTERY","searchapi/CATALOG_PAUSED_REASON_LOW_DISK","searchapi/CATALOG_PAUSED_REASON_LOW_MEMORY","searchapi/CATALOG_PAUSED_REASON_NONE","searchapi/CATALOG_PAUSED_REASON_UPGRADING","searchapi/CATALOG_PAUSED_REASON_USER_ACTIVE","searchapi/CatalogPausedReason"]
old-location: search\_search_CatalogPausedReason.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\catalogpausedreason.htm
ms.date: 12/05/2018
ms.keywords: CATALOG_PAUSED_REASON_DELAYED_RECOVERY, CATALOG_PAUSED_REASON_EXTERNAL, CATALOG_PAUSED_REASON_HIGH_CPU, CATALOG_PAUSED_REASON_HIGH_IO, CATALOG_PAUSED_REASON_HIGH_NTF_RATE, CATALOG_PAUSED_REASON_LOW_BATTERY, CATALOG_PAUSED_REASON_LOW_DISK, CATALOG_PAUSED_REASON_LOW_MEMORY, CATALOG_PAUSED_REASON_NONE, CATALOG_PAUSED_REASON_UPGRADING, CATALOG_PAUSED_REASON_USER_ACTIVE, CatalogPausedReason, CatalogPausedReason enumeration [search], _search_CatalogPausedReason, search._search_CatalogPausedReason, searchapi/CATALOG_PAUSED_REASON_DELAYED_RECOVERY, searchapi/CATALOG_PAUSED_REASON_EXTERNAL, searchapi/CATALOG_PAUSED_REASON_HIGH_CPU, searchapi/CATALOG_PAUSED_REASON_HIGH_IO, searchapi/CATALOG_PAUSED_REASON_HIGH_NTF_RATE, searchapi/CATALOG_PAUSED_REASON_LOW_BATTERY, searchapi/CATALOG_PAUSED_REASON_LOW_DISK, searchapi/CATALOG_PAUSED_REASON_LOW_MEMORY, searchapi/CATALOG_PAUSED_REASON_NONE, searchapi/CATALOG_PAUSED_REASON_UPGRADING, searchapi/CATALOG_PAUSED_REASON_USER_ACTIVE, searchapi/CatalogPausedReason
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchcatalog.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CatalogPausedReason
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CatalogPausedReason
 - searchapi/_CatalogPausedReason
 - CatalogPausedReason
 - searchapi/CatalogPausedReason
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
 - CatalogPausedReason
---

# CatalogPausedReason enumeration


## -description

Used by <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus">ISearchCatalogManager::GetCatalogStatus</a> to determine the reason the catalog is paused.

## -enum-fields

### -field CATALOG_PAUSED_REASON_NONE:0

Not paused.

### -field CATALOG_PAUSED_REASON_HIGH_IO:1

Paused due to high I/O.

### -field CATALOG_PAUSED_REASON_HIGH_CPU:2

Paused due to high CPU usage.

### -field CATALOG_PAUSED_REASON_HIGH_NTF_RATE:3

Paused due to high NTF rate.

### -field CATALOG_PAUSED_REASON_LOW_BATTERY:4

Paused due to low battery.

### -field CATALOG_PAUSED_REASON_LOW_MEMORY:5

Paused due to low memory.

### -field CATALOG_PAUSED_REASON_LOW_DISK:6

Paused due to low disk space.

### -field CATALOG_PAUSED_REASON_DELAYED_RECOVERY:7

Paused due to need for delayed recovery.

### -field CATALOG_PAUSED_REASON_USER_ACTIVE:8

Paused due to user activity.

### -field CATALOG_PAUSED_REASON_EXTERNAL:9

Paused by external request.

### -field CATALOG_PAUSED_REASON_UPGRADING:10

Paused by upgrading.
