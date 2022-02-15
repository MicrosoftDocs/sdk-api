---
UID: NE:shobjidl_core.SYNC_TRANSFER_STATUS
title: SYNC_TRANSFER_STATUS (shobjidl_core.h)
description: Specifies possible status values used in the System.SyncTransferStatus property.
helpviewer_keywords: ["STS_FETCHING_METADATA","STS_HASERROR","STS_NEEDSDOWNLOAD","STS_NEEDSUPLOAD","STS_NONE","STS_PAUSED","STS_TRANSFERRING","SYNC_TRANSFER_STATUS","SYNC_TRANSFER_STATUS enumeration [Windows Properties]","properties.SYNC_TRANSFER_STATUS","shobjidl_core/STS_FETCHING_METADATA","shobjidl_core/STS_HASERROR","shobjidl_core/STS_NEEDSDOWNLOAD","shobjidl_core/STS_NEEDSUPLOAD","shobjidl_core/STS_NONE","shobjidl_core/STS_PAUSED","shobjidl_core/STS_TRANSFERRING","shobjidl_core/SYNC_TRANSFER_STATUS"]
old-location: properties\SYNC_TRANSFER_STATUS.htm
tech.root: properties
ms.assetid: B772BF05-0E82-48E6-9A0B-A3C53FBC5F60
ms.date: 12/05/2018
ms.keywords: STS_FETCHING_METADATA, STS_HASERROR, STS_NEEDSDOWNLOAD, STS_NEEDSUPLOAD, STS_NONE, STS_PAUSED, STS_TRANSFERRING, SYNC_TRANSFER_STATUS, SYNC_TRANSFER_STATUS enumeration [Windows Properties], properties.SYNC_TRANSFER_STATUS, shobjidl_core/STS_FETCHING_METADATA, shobjidl_core/STS_HASERROR, shobjidl_core/STS_NEEDSDOWNLOAD, shobjidl_core/STS_NEEDSUPLOAD, shobjidl_core/STS_NONE, shobjidl_core/STS_PAUSED, shobjidl_core/STS_TRANSFERRING, shobjidl_core/SYNC_TRANSFER_STATUS
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
targetos: Windows
req.typenames: SYNC_TRANSFER_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYNC_TRANSFER_STATUS
 - shobjidl_core/SYNC_TRANSFER_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - SYNC_TRANSFER_STATUS
---

# SYNC_TRANSFER_STATUS enumeration


## -description

Specifies possible status values used in the System.SyncTransferStatus property.

## -enum-fields

### -field STS_NONE:0

There is no current sync activity.

### -field STS_NEEDSUPLOAD:0x1

The file is pending upload.

### -field STS_NEEDSDOWNLOAD:0x2

The file is pending download.

### -field STS_TRANSFERRING:0x4

The file is currently being uploaded or downloaded.

### -field STS_PAUSED:0x8

The current transfer is paused.

### -field STS_HASERROR:0x10

An error was encountered during the last sync operation.

### -field STS_FETCHING_METADATA:0x20

The sync engine is retrieving metadata from the cloud.

### -field STS_USER_REQUESTED_REFRESH:0x40

### -field STS_HASWARNING:0x80

### -field STS_EXCLUDED:0x100

### -field STS_INCOMPLETE:0x200

### -field STS_PLACEHOLDER_IFEMPTY:0x400

