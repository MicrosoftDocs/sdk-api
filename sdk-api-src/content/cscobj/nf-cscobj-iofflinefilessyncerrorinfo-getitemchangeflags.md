---
UID: NF:cscobj.IOfflineFilesSyncErrorInfo.GetItemChangeFlags
title: IOfflineFilesSyncErrorInfo::GetItemChangeFlags (cscobj.h)
description: Retrieves a value containing a set of flags that describe what changes were encountered during the sync operation associated with the sync error.
helpviewer_keywords: ["GetItemChangeFlags","GetItemChangeFlags method [Offline Files]","GetItemChangeFlags method [Offline Files]","IOfflineFilesSyncErrorInfo interface","IOfflineFilesSyncErrorInfo interface [Offline Files]","GetItemChangeFlags method","IOfflineFilesSyncErrorInfo.GetItemChangeFlags","IOfflineFilesSyncErrorInfo::GetItemChangeFlags","OFFLINEFILES_SYNC_ITEM_CHANGE_ATTRIBUTES","OFFLINEFILES_SYNC_ITEM_CHANGE_CHANGETIME","OFFLINEFILES_SYNC_ITEM_CHANGE_FILESIZE","OFFLINEFILES_SYNC_ITEM_CHANGE_NONE","OFFLINEFILES_SYNC_ITEM_CHANGE_WRITETIME","cscobj/IOfflineFilesSyncErrorInfo::GetItemChangeFlags","of.iofflinefilessyncerrorinfo_getitemchangeflags"]
old-location: of\iofflinefilessyncerrorinfo_getitemchangeflags.htm
tech.root: of
ms.assetid: 1014e42f-83af-493e-b264-a46055f646a5
ms.date: 12/05/2018
ms.keywords: GetItemChangeFlags, GetItemChangeFlags method [Offline Files], GetItemChangeFlags method [Offline Files],IOfflineFilesSyncErrorInfo interface, IOfflineFilesSyncErrorInfo interface [Offline Files],GetItemChangeFlags method, IOfflineFilesSyncErrorInfo.GetItemChangeFlags, IOfflineFilesSyncErrorInfo::GetItemChangeFlags, OFFLINEFILES_SYNC_ITEM_CHANGE_ATTRIBUTES, OFFLINEFILES_SYNC_ITEM_CHANGE_CHANGETIME, OFFLINEFILES_SYNC_ITEM_CHANGE_FILESIZE, OFFLINEFILES_SYNC_ITEM_CHANGE_NONE, OFFLINEFILES_SYNC_ITEM_CHANGE_WRITETIME, cscobj/IOfflineFilesSyncErrorInfo::GetItemChangeFlags, of.iofflinefilessyncerrorinfo_getitemchangeflags
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesSyncErrorInfo::GetItemChangeFlags
 - cscobj/IOfflineFilesSyncErrorInfo::GetItemChangeFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSyncErrorInfo.GetItemChangeFlags
---

# IOfflineFilesSyncErrorInfo::GetItemChangeFlags


## -description

Retrieves a value containing a set of flags that describe what changes were encountered during the sync operation associated with the sync error.

## -parameters

### -param pdwItemChangeFlags [out]

Receives a set of flags describing what changes were encountered during the sync operation.  This parameter can be one or more of the following flag values:



#### OFFLINEFILES_SYNC_ITEM_CHANGE_NONE (0x00000000)

No changes were detected.



#### OFFLINEFILES_SYNC_ITEM_CHANGE_CHANGETIME (0x00000001)

The item's last-change time was found to be different between client and server.



#### OFFLINEFILES_SYNC_ITEM_CHANGE_WRITETIME (0x00000002)

The item's write time was found to be different between client and server.



#### OFFLINEFILES_SYNC_ITEM_CHANGE_FILESIZE (0x00000004)

The item's size was found to be different between client and server.



#### OFFLINEFILES_SYNC_ITEM_CHANGE_ATTRIBUTES (0x00000008)

One or more of the item's attributes were found to be different between client and server.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerrorinfo">IOfflineFilesSyncErrorInfo</a>