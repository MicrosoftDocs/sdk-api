---
UID: NE:cscobj.tagOFFLINEFILES_ITEM_TYPE
title: tagOFFLINEFILES_ITEM_TYPE
author: windows-driver-content
description: Identifies the type of an item in the Offline Files cache.
old-location: of\offlinefiles_item_type.htm
old-project: OfflineFiles
ms.assetid: cf8bb079-d691-4b37-b408-d1af1746ed37
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: OFFLINEFILES_ITEM_TYPE, OFFLINEFILES_ITEM_TYPE enumeration [Offline Files], OFFLINEFILES_ITEM_TYPE_DIRECTORY, OFFLINEFILES_ITEM_TYPE_FILE, OFFLINEFILES_ITEM_TYPE_SERVER, OFFLINEFILES_ITEM_TYPE_SHARE, cscobj/OFFLINEFILES_ITEM_TYPE, cscobj/OFFLINEFILES_ITEM_TYPE_DIRECTORY, cscobj/OFFLINEFILES_ITEM_TYPE_FILE, cscobj/OFFLINEFILES_ITEM_TYPE_SERVER, cscobj/OFFLINEFILES_ITEM_TYPE_SHARE, of.offlinefiles_item_type, tagOFFLINEFILES_ITEM_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: OFFLINEFILES_ITEM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CscObj.h
api_name:
-	OFFLINEFILES_ITEM_TYPE
product: Windows
targetos: Windows
req.lib: CscApi.lib
req.dll: CscApi.dll
req.irql: 
---

# tagOFFLINEFILES_ITEM_TYPE enumeration


## -description


Identifies the type of an item in the Offline Files cache.


## -enum-fields




### -field OFFLINEFILES_ITEM_TYPE_FILE

The item is a file.


### -field OFFLINEFILES_ITEM_TYPE_DIRECTORY

The item is a directory.


### -field OFFLINEFILES_ITEM_TYPE_SHARE

The item is a share.


### -field OFFLINEFILES_ITEM_TYPE_SERVER

The item is a server.


## -see-also




<a href="https://msdn.microsoft.com/9300b4f3-1261-40d2-ae05-fb1be2f857b9">IOfflineFilesDirectoryItem</a>



<a href="https://msdn.microsoft.com/53b9af4b-7526-4b54-bae2-61c97aa67ebf">IOfflineFilesFileItem</a>



<a href="https://msdn.microsoft.com/870cf4c4-e757-429d-b6cc-c136ed5aa10e">IOfflineFilesItem</a>



<a href="https://msdn.microsoft.com/87fbf63a-d103-4c80-b6a7-60784c7350bc">IOfflineFilesItem::GetItemType</a>



<a href="https://msdn.microsoft.com/724fabf6-fb27-49c9-8f99-dc61377ac921">IOfflineFilesServerItem</a>



<a href="https://msdn.microsoft.com/aff6be4a-07bc-4a74-8fbf-92fe8985f5b6">IOfflineFilesShareItem</a>
 

 

