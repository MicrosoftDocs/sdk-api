---
UID: NE:searchapi._CatalogPausedReason
title: "_CatalogPausedReason"
author: windows-sdk-content
description: Used by ISearchCatalogManager::GetCatalogStatus to determine the reason the catalog is paused.
old-location: search\_search_CatalogPausedReason.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\catalogpausedreason.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CATALOG_PAUSED_REASON_DELAYED_RECOVERY, CATALOG_PAUSED_REASON_EXTERNAL, CATALOG_PAUSED_REASON_HIGH_CPU, CATALOG_PAUSED_REASON_HIGH_IO, CATALOG_PAUSED_REASON_HIGH_NTF_RATE, CATALOG_PAUSED_REASON_LOW_BATTERY, CATALOG_PAUSED_REASON_LOW_DISK, CATALOG_PAUSED_REASON_LOW_MEMORY, CATALOG_PAUSED_REASON_NONE, CATALOG_PAUSED_REASON_UPGRADING, CATALOG_PAUSED_REASON_USER_ACTIVE, CatalogPausedReason, CatalogPausedReason enumeration [search], _CatalogPausedReason, _search_CatalogPausedReason, search._search_CatalogPausedReason, searchapi/CATALOG_PAUSED_REASON_DELAYED_RECOVERY, searchapi/CATALOG_PAUSED_REASON_EXTERNAL, searchapi/CATALOG_PAUSED_REASON_HIGH_CPU, searchapi/CATALOG_PAUSED_REASON_HIGH_IO, searchapi/CATALOG_PAUSED_REASON_HIGH_NTF_RATE, searchapi/CATALOG_PAUSED_REASON_LOW_BATTERY, searchapi/CATALOG_PAUSED_REASON_LOW_DISK, searchapi/CATALOG_PAUSED_REASON_LOW_MEMORY, searchapi/CATALOG_PAUSED_REASON_NONE, searchapi/CATALOG_PAUSED_REASON_UPGRADING, searchapi/CATALOG_PAUSED_REASON_USER_ACTIVE, searchapi/CatalogPausedReason
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
req.idl: Searchcatalog.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CatalogPausedReason
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Searchapi.h
api_name:
-	CatalogPausedReason
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _CatalogPausedReason enumeration


## -description


Used by <a href="https://msdn.microsoft.com/22cd866e-8af7-428a-8036-43f5ac9ad099">ISearchCatalogManager::GetCatalogStatus</a> to determine the reason the catalog is paused.


## -enum-fields




### -field CATALOG_PAUSED_REASON_NONE

Not paused.


### -field CATALOG_PAUSED_REASON_HIGH_IO

Paused due to high I/O.


### -field CATALOG_PAUSED_REASON_HIGH_CPU

Paused due to high CPU usage.


### -field CATALOG_PAUSED_REASON_HIGH_NTF_RATE

Paused due to high NTF rate.


### -field CATALOG_PAUSED_REASON_LOW_BATTERY

Paused due to low battery.


### -field CATALOG_PAUSED_REASON_LOW_MEMORY

Paused due to low memory.


### -field CATALOG_PAUSED_REASON_LOW_DISK

Paused due to low disk space.


### -field CATALOG_PAUSED_REASON_DELAYED_RECOVERY

Paused due to need for delayed recovery.


### -field CATALOG_PAUSED_REASON_USER_ACTIVE

Paused due to user activity.


### -field CATALOG_PAUSED_REASON_EXTERNAL

Paused by external request.


### -field CATALOG_PAUSED_REASON_UPGRADING

Paused by upgrading.

