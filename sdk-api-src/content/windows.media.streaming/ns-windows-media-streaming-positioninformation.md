---
UID: NS:windows.media.streaming.PositionInformation
title: PositionInformation (windows.media.streaming.h)
description: Contains the current values of media playback position information obtained from the DMR.
helpviewer_keywords: ["PositionInformation","PositionInformation structure [Media Streaming API]","mediastreaming.positioninformation","windows/PositionInformation"]
old-location: mediastreaming\positioninformation.htm
tech.root: mediastreaming
ms.assetid: 9601c1ae-3fd2-4761-8aa7-102b72ef4733
ms.date: 12/05/2018
ms.keywords: PositionInformation, PositionInformation structure [Media Streaming API], mediastreaming.positioninformation, windows/PositionInformation
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
req.typenames: PositionInformation
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PositionInformation
 - windows.media.streaming/PositionInformation
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
 - PositionInformation
---

# PositionInformation structure


## -description

Contains the current values of media playback position information obtained from the DMR.

## -struct-fields

### -field streaming.PositionInformation.trackInformation

### -field streaming.PositionInformation.relativeTime

### -field relativeTime

The current playback position of the DMR.

### -field trackInformation

A <a href="/previous-versions/windows/desktop/legacy/hh829004(v=vs.85)">TrackInformation</a> structure that contains the current track number and duration.