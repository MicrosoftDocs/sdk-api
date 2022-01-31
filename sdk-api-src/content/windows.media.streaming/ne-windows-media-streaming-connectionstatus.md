---
UID: NE:windows.media.streaming.ConnectionStatus
title: ConnectionStatus (windows.media.streaming.h)
description: Represents the state of the device in the network as last seen.
helpviewer_keywords: ["ConnectionStatus","ConnectionStatus enumeration [Media Streaming API]","Offline","Online","Sleeping","mediastreaming.connectionstatus","windows/ConnectionStatus","windows/Offline","windows/Online","windows/Sleeping"]
old-location: mediastreaming\connectionstatus.htm
tech.root: mediastreaming
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
ms.date: 12/05/2018
ms.keywords: ConnectionStatus, ConnectionStatus enumeration [Media Streaming API], Offline, Online, Sleeping, mediastreaming.connectionstatus, windows/ConnectionStatus, windows/Offline, windows/Online, windows/Sleeping
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
 - ConnectionStatus
 - windows.media.streaming/ConnectionStatus
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
 - ConnectionStatus
---

# ConnectionStatus enumeration


## -description

Represents the state of the device in the network as last seen.

## -enum-fields

### -field ConnectionStatus_Online:0

### -field ConnectionStatus_Offline:1

### -field ConnectionStatus_Sleeping:2

#### - Offline

Device is offline.


#### - Online

Device is online and active on the network.


#### - Sleeping

Device is currently offline but might automatically wake up when an attempt is made to communicate with it.

