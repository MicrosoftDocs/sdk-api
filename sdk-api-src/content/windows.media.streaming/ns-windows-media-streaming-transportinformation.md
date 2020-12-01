---
UID: NS:windows.media.streaming.TransportInformation
title: TransportInformation (windows.media.streaming.h)
description: Contains the current values of media playback transport-related information obtained from the DMR.
helpviewer_keywords: ["TransportInformation","TransportInformation structure [Media Streaming API]","mediastreaming.transportinformation","windows/TransportInformation"]
old-location: mediastreaming\transportinformation.htm
tech.root: mediastreaming
ms.assetid: c91f84f2-e19b-4bfa-862d-fc5e1dc756d4
ms.date: 12/05/2018
ms.keywords: TransportInformation, TransportInformation structure [Media Streaming API], mediastreaming.transportinformation, windows/TransportInformation
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
req.typenames: TransportInformation
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TransportInformation
 - windows.media.streaming/TransportInformation
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
 - TransportInformation
---

# TransportInformation structure


## -description

Contains the current values of media playback transport-related information obtained from the DMR.

## -struct-fields

### -field streaming.TransportInformation.CurrentTransportState

### -field streaming.TransportInformation.CurrentTransportStatus

### -field streaming.TransportInformation.CurrentSpeed

### -field CurrentSpeed

A <a href="/previous-versions/windows/desktop/legacy/hh828990(v=vs.85)">PlaySpeed</a> structure, indicating the current speed at which the DMR is playing the content, or was last playing the content.

### -field CurrentTransportState

A value from the <a href="/windows/desktop/mediastreaming/transportstate">TransportState</a> enumeration, indicating the current transport state of the DMR.

### -field CurrentTransportStatus

A value from the <a href="/windows/desktop/mediastreaming/transportstatus">TransportStatus</a> enumeration, indicating the current transport status reported by the DMR.