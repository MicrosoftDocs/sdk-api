---
UID: NS:windows.media.streaming.RenderingParameters
title: RenderingParameters (windows.media.streaming.h)
description: Contains the current values of rendering parameters on the DMR.
helpviewer_keywords: ["RenderingParameters","RenderingParameters structure [Media Streaming API]","mediastreaming.renderingparameters","windows/RenderingParameters"]
old-location: mediastreaming\renderingparameters.htm
tech.root: mediastreaming
ms.assetid: d5a558e1-75c3-4276-a6e7-4b688f871031
ms.date: 12/05/2018
ms.keywords: RenderingParameters, RenderingParameters structure [Media Streaming API], mediastreaming.renderingparameters, windows/RenderingParameters
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
req.typenames: RenderingParameters
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RenderingParameters
 - windows.media.streaming/RenderingParameters
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
 - RenderingParameters
---

# RenderingParameters structure


## -description

Contains the current values of rendering parameters on the DMR.

## -struct-fields

### -field streaming.RenderingParameters.volume

### -field streaming.RenderingParameters.mute

### -field mute

This value is <b>True</b> if audio is currently muted on the DMR, and is <b>False</b> otherwise.

### -field volume

The current audio volume level of the device, in the range 0 to 100, or -1 if the device does not support controlling the volume level.  A value of 0 is the lowest volume and a value of 100 is the highest.

