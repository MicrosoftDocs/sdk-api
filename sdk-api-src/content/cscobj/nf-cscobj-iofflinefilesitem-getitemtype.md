---
UID: NF:cscobj.IOfflineFilesItem.GetItemType
title: IOfflineFilesItem::GetItemType (cscobj.h)
author: windows-sdk-content
description: Returns a type code identifying the type of the item:\_server, share, directory, or file.
old-location: of\iofflinefilesitem_getitemtype.htm
tech.root: offlinefiles
ms.assetid: 87fbf63a-d103-4c80-b6a7-60784c7350bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetItemType, GetItemType method [Offline Files], GetItemType method [Offline Files],IOfflineFilesItem interface, IOfflineFilesItem interface [Offline Files],GetItemType method, IOfflineFilesItem.GetItemType, IOfflineFilesItem::GetItemType, cscobj/IOfflineFilesItem::GetItemType, of.iofflinefilesitem_getitemtype
ms.topic: method
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesItem.GetItemType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesItem::GetItemType


## -description


Returns a type code identifying the type of the item: server, share, directory, or file.


## -parameters




### -param pItemType [out]

Receives an <a href="https://msdn.microsoft.com/cf8bb079-d691-4b37-b408-d1af1746ed37">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



Another way to determine an item's type is to query the item for one of the following type-specific interfaces:

<a href="https://msdn.microsoft.com/9300b4f3-1261-40d2-ae05-fb1be2f857b9">IOfflineFilesDirectoryItem</a>
<a href="https://msdn.microsoft.com/53b9af4b-7526-4b54-bae2-61c97aa67ebf">IOfflineFilesFileItem</a>
<a href="https://msdn.microsoft.com/724fabf6-fb27-49c9-8f99-dc61377ac921">IOfflineFilesServerItem</a>
<a href="https://msdn.microsoft.com/aff6be4a-07bc-4a74-8fbf-92fe8985f5b6">IOfflineFilesShareItem</a>
If the call to <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> succeeds, the item is of the requested type.  An item can be of only one of the above types.




## -see-also




<a href="https://msdn.microsoft.com/870cf4c4-e757-429d-b6cc-c136ed5aa10e">IOfflineFilesItem</a>
 

 

