---
UID: NE:windows.media.streaming.ConnectionStatus
title: ConnectionStatus (windows.media.streaming.h)
author: windows-sdk-content
description: Represents the state of the device in the network as last seen.
old-location: mediastreaming\connectionstatus.htm
tech.root: mediastreaming
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ConnectionStatus, ConnectionStatus enumeration [Media Streaming API], Offline, Online, Sleeping, mediastreaming.connectionstatus, windows/ConnectionStatus, windows/Offline, windows/Online, windows/Sleeping
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
 - ConnectionStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ConnectionStatus enumeration


## -description


Represents the state of the device in the network as last seen.


## -enum-fields




### -field ConnectionStatus_Online


### -field ConnectionStatus_Offline


### -field ConnectionStatus_Sleeping




#### - Offline

Device is offline.


#### - Online

Device is online and active on the network.


#### - Sleeping

Device is currently offline but might automatically wake up when an attempt is made to communicate with it.

