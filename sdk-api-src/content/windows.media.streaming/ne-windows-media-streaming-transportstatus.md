---
UID: NE:windows.media.streaming.TransportStatus
title: TransportStatus (windows.media.streaming.h)
description: Defines the available transport status as defined by the UPnP Guidelines.
helpviewer_keywords: ["ErrorOccurred","Last","Ok","TransportStatus","TransportStatus enumeration [Media Streaming API]","Unknown","mediastreaming.transportstatus","windows/ErrorOccurred","windows/Last","windows/Ok","windows/TransportStatus","windows/Unknown"]
old-location: mediastreaming\transportstatus.htm
tech.root: mediastreaming
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
ms.date: 12/05/2018
ms.keywords: ErrorOccurred, Last, Ok, TransportStatus, TransportStatus enumeration [Media Streaming API], Unknown, mediastreaming.transportstatus, windows/ErrorOccurred, windows/Last, windows/Ok, windows/TransportStatus, windows/Unknown
req.header: windows.media.streaming.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TransportStatus
 - windows.media.streaming/TransportStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windows.media.streaming.h
api_name:
 - TransportStatus
---

# TransportStatus enumeration


## -description

Defines the available transport status as defined by the UPnP Guidelines.

## -enum-fields

### -field TransportStatus_Unknown:0

### -field TransportStatus_Ok:1

### -field TransportStatus_ErrorOccurred:2

### -field TransportStatus_Last:3

#### - ErrorOccurred

An error occurred on the device.


#### - Last

The device’s previous status to the current transport status.


#### - Ok

The device is in a good status.


#### - Unknown

Erroneous device status.

