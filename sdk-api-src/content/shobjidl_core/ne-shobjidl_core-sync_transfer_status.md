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



