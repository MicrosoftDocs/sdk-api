---
UID: NE:cscobj.tagOFFLINEFILES_ITEM_TIME
title: OFFLINEFILES_ITEM_TIME (cscobj.h)
description: Specifies which time value associated with the cache item is to be used.
helpviewer_keywords: ["OFFLINEFILES_ITEM_TIME","OFFLINEFILES_ITEM_TIME enumeration [Offline Files]","OFFLINEFILES_ITEM_TIME_CREATION","OFFLINEFILES_ITEM_TIME_LASTACCESS","OFFLINEFILES_ITEM_TIME_LASTWRITE","cscobj/OFFLINEFILES_ITEM_TIME","cscobj/OFFLINEFILES_ITEM_TIME_CREATION","cscobj/OFFLINEFILES_ITEM_TIME_LASTACCESS","cscobj/OFFLINEFILES_ITEM_TIME_LASTWRITE","of.offlinefiles_item_time"]
old-location: of\offlinefiles_item_time.htm
tech.root: of
ms.assetid: 14fd41fe-c5d9-4381-8ced-7ebe183fb30c
ms.date: 12/05/2018
ms.keywords: OFFLINEFILES_ITEM_TIME, OFFLINEFILES_ITEM_TIME enumeration [Offline Files], OFFLINEFILES_ITEM_TIME_CREATION, OFFLINEFILES_ITEM_TIME_LASTACCESS, OFFLINEFILES_ITEM_TIME_LASTWRITE, cscobj/OFFLINEFILES_ITEM_TIME, cscobj/OFFLINEFILES_ITEM_TIME_CREATION, cscobj/OFFLINEFILES_ITEM_TIME_LASTACCESS, cscobj/OFFLINEFILES_ITEM_TIME_LASTWRITE, of.offlinefiles_item_time
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OFFLINEFILES_ITEM_TIME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOFFLINEFILES_ITEM_TIME
 - cscobj/tagOFFLINEFILES_ITEM_TIME
 - OFFLINEFILES_ITEM_TIME
 - cscobj/OFFLINEFILES_ITEM_TIME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CscObj.h
api_name:
 - OFFLINEFILES_ITEM_TIME
---

# OFFLINEFILES_ITEM_TIME enumeration


## -description

Specifies which time value associated with the cache item is to be used.

## -enum-fields

### -field OFFLINEFILES_ITEM_TIME_CREATION:0

Use the item's creation time.

### -field OFFLINEFILES_ITEM_TIME_LASTACCESS

Use the item's last-access time.

### -field OFFLINEFILES_ITEM_TIME_LASTWRITE

Use the item's last-write time.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitemfilter-gettimefilter">IOfflineFilesItemFilter::GetTimeFilter</a>
