---
UID: NE:cscobj.tagOFFLINEFILES_ITEM_TYPE
title: OFFLINEFILES_ITEM_TYPE (cscobj.h)
description: Identifies the type of an item in the Offline Files cache.
helpviewer_keywords: ["OFFLINEFILES_ITEM_TYPE","OFFLINEFILES_ITEM_TYPE enumeration [Offline Files]","OFFLINEFILES_ITEM_TYPE_DIRECTORY","OFFLINEFILES_ITEM_TYPE_FILE","OFFLINEFILES_ITEM_TYPE_SERVER","OFFLINEFILES_ITEM_TYPE_SHARE","cscobj/OFFLINEFILES_ITEM_TYPE","cscobj/OFFLINEFILES_ITEM_TYPE_DIRECTORY","cscobj/OFFLINEFILES_ITEM_TYPE_FILE","cscobj/OFFLINEFILES_ITEM_TYPE_SERVER","cscobj/OFFLINEFILES_ITEM_TYPE_SHARE","of.offlinefiles_item_type"]
old-location: of\offlinefiles_item_type.htm
tech.root: of
ms.assetid: cf8bb079-d691-4b37-b408-d1af1746ed37
ms.date: 12/05/2018
ms.keywords: OFFLINEFILES_ITEM_TYPE, OFFLINEFILES_ITEM_TYPE enumeration [Offline Files], OFFLINEFILES_ITEM_TYPE_DIRECTORY, OFFLINEFILES_ITEM_TYPE_FILE, OFFLINEFILES_ITEM_TYPE_SERVER, OFFLINEFILES_ITEM_TYPE_SHARE, cscobj/OFFLINEFILES_ITEM_TYPE, cscobj/OFFLINEFILES_ITEM_TYPE_DIRECTORY, cscobj/OFFLINEFILES_ITEM_TYPE_FILE, cscobj/OFFLINEFILES_ITEM_TYPE_SERVER, cscobj/OFFLINEFILES_ITEM_TYPE_SHARE, of.offlinefiles_item_type
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
req.typenames: OFFLINEFILES_ITEM_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOFFLINEFILES_ITEM_TYPE
 - cscobj/tagOFFLINEFILES_ITEM_TYPE
 - OFFLINEFILES_ITEM_TYPE
 - cscobj/OFFLINEFILES_ITEM_TYPE
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
 - OFFLINEFILES_ITEM_TYPE
---

# OFFLINEFILES_ITEM_TYPE enumeration


## -description

Identifies the type of an item in the Offline Files cache.

## -enum-fields

### -field OFFLINEFILES_ITEM_TYPE_FILE:0

The item is a file.

### -field OFFLINEFILES_ITEM_TYPE_DIRECTORY

The item is a directory.

### -field OFFLINEFILES_ITEM_TYPE_SHARE

The item is a share.

### -field OFFLINEFILES_ITEM_TYPE_SERVER

The item is a server.

## -see-also

<a href="/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesdirectoryitem">IOfflineFilesDirectoryItem</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesfileitem">IOfflineFilesFileItem</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitem-getitemtype">IOfflineFilesItem::GetItemType</a>



<a href="/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesserveritem">IOfflineFilesServerItem</a>



<a href="/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesshareitem">IOfflineFilesShareItem</a>
