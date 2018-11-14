---
UID: NE:windows.media.streaming.TransportStatus
title: TransportStatus
author: windows-sdk-content
description: Defines the available transport status as defined by the UPnP Guidelines.
old-location: mediastreaming\transportstatus.htm
tech.root: mediastreaming
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ErrorOccurred, Last, Ok, TransportStatus, TransportStatus enumeration [Media Streaming API], Unknown, mediastreaming.transportstatus, windows/ErrorOccurred, windows/Last, windows/Ok, windows/TransportStatus, windows/Unknown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windows.media.streaming.h
api_name:
 - TransportStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TransportStatus enumeration


## -description


Defines the available transport status as defined by the UPnP Guidelines.


## -enum-fields




### -field TransportStatus_Unknown


### -field TransportStatus_Ok


### -field TransportStatus_ErrorOccurred


### -field TransportStatus_Last


### -field int




#### - ErrorOccurred

An error occurred on the device.


#### - Last

The device’s previous status to the current transport status.


#### - Ok

The device is in a good status.


#### - Unknown

Erroneous device status.

