---
UID: NS:windows.media.streaming.PlaySpeed
title: PlaySpeed (windows.media.streaming.h)
description: Represents a playback speed as a rational number.
helpviewer_keywords: ["PlaySpeed","PlaySpeed structure [Media Streaming API]","mediastreaming.playspeed","windows/PlaySpeed"]
old-location: mediastreaming\playspeed.htm
tech.root: mediastreaming
ms.assetid: 29b58229-8236-4c93-a6b4-ed09d1aca9db
ms.date: 12/05/2018
ms.keywords: PlaySpeed, PlaySpeed structure [Media Streaming API], mediastreaming.playspeed, windows/PlaySpeed
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
req.typenames: PlaySpeed
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PlaySpeed
 - windows.media.streaming/PlaySpeed
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
 - PlaySpeed
---

# PlaySpeed structure


## -description

Represents a playback speed as a rational number.

## -struct-fields

### -field streaming.PlaySpeed.Numerator

### -field streaming.PlaySpeed.Denominator

### -field Denominator

The <b>Numerator</b> should be divided by this value to obtain the play speed.  A value of 0 is not allowed.

### -field Numerator

A value that when divided by the <b>Denominator</b> represents the play speed.

## -remarks

The <b>Numerator</b> is a signed integer, allowing for negative speeds.  A negative speed means that the content is played in reverse.  A speed of 1 means that the content is played at its normal playback speed.

