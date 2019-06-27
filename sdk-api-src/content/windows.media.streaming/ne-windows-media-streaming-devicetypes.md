---
UID: NE:windows.media.streaming.DeviceTypes
title: DeviceTypes (windows.media.streaming.h)
author: windows-sdk-content
description: Describes the DLNA device types that are supported by the Media Streaming API.
old-location: mediastreaming\devicetypes.htm
tech.root: mediastreaming
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeviceTypes, DeviceTypes enumeration [Media Streaming API], DigitalMediaPlayer, DigitalMediaRenderer, DigitalMediaServer, Unknown, mediastreaming.devicetypes, windows/DeviceTypes, windows/DigitalMediaPlayer, windows/DigitalMediaRenderer, windows/DigitalMediaServer, windows/Unknown
ms.topic: enum
f1_keywords: 
 - "windows.media.streaming/DeviceTypes"
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
 - DeviceTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeviceTypes enumeration


## -description


Describes the DLNA device types that are supported by the Media Streaming API.


## -enum-fields




### -field DeviceTypes_Unknown


### -field DeviceTypes_DigitalMediaRenderer


### -field DeviceTypes_DigitalMediaServer


### -field DeviceTypes_DigitalMediaPlayer




#### - DigitalMediaPlayer

DLNA Digital Media Player


#### - DigitalMediaRenderer

DLNA Digital Media Renderer (DMR). The value is equivalent to the device type <b>urn:schemas-upnp-org:device:MediaRenderer:1</b>.


#### - DigitalMediaServer

DLNA Digital Media Server (DMS). The value is equivalent to the device type <b>urn:schemas-upnp-org:device:MediaServer:1</b>.


#### - Unknown

Unknown device type.

