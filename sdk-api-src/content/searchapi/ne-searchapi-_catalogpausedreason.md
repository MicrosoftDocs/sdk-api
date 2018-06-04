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

