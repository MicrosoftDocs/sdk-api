---
UID: NE:shobjidl_core.SYNC_TRANSFER_STATUS
title: SYNC_TRANSFER_STATUS (shobjidl_core.h)

description: Specifies possible status values used in the System.SyncTransferStatus property.
old-location: properties\SYNC_TRANSFER_STATUS.htm
tech.root: properties
ms.assetid: B772BF05-0E82-48E6-9A0B-A3C53FBC5F60

ms.date: 12/05/2018
ms.keywords: STS_FETCHING_METADATA, STS_HASERROR, STS_NEEDSDOWNLOAD, STS_NEEDSUPLOAD, STS_NONE, STS_PAUSED, STS_TRANSFERRING, SYNC_TRANSFER_STATUS, SYNC_TRANSFER_STATUS enumeration [Windows Properties], properties.SYNC_TRANSFER_STATUS, shobjidl_core/STS_FETCHING_METADATA, shobjidl_core/STS_HASERROR, shobjidl_core/STS_NEEDSDOWNLOAD, shobjidl_core/STS_NEEDSUPLOAD, shobjidl_core/STS_NONE, shobjidl_core/STS_PAUSED, shobjidl_core/STS_TRANSFERRING, shobjidl_core/SYNC_TRANSFER_STATUS
ms.topic: enum
f1_keywords: 
 - "shobjidl_core/SYNC_TRANSFER_STATUS"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - SYNC_TRANSFER_STATUS
targetos: Windows
req.typenames: SYNC_TRANSFER_STATUS
req.redist: 
ms.custom: 19H1
---

# SYNC_TRANSFER_STATUS enumeration


## -description


Specifies possible status values used in the System.SyncTransferStatus property.


## -enum-fields




### -field STS_NONE

There is no current sync activity.


### -field STS_NEEDSUPLOAD

The file is pending upload.


### -field STS_NEEDSDOWNLOAD

The file is pending download.


### -field STS_TRANSFERRING

The file is currently being uploaded or downloaded.


### -field STS_PAUSED

The current transfer is paused.


### -field STS_HASERROR

An error was encountered during the last sync operation.


### -field STS_FETCHING_METADATA

The sync engine is retrieving metadata from the cloud.


### -field STS_USER_REQUESTED_REFRESH


### -field STS_HASWARNING


### -field STS_EXCLUDED


### -field STS_INCOMPLETE


### -field STS_PLACEHOLDER_IFEMPTY



