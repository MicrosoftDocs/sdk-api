---
UID: NS:windows.media.streaming.PlaySpeed
title: PlaySpeed (windows.media.streaming.h)
author: windows-sdk-content
description: Represents a playback speed as a rational number.
old-location: mediastreaming\playspeed.htm
tech.root: mediastreaming
ms.assetid: 29b58229-8236-4c93-a6b4-ed09d1aca9db
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PlaySpeed, PlaySpeed structure [Media Streaming API], mediastreaming.playspeed, windows/PlaySpeed
ms.topic: struct
f1_keywords: 
 - "windows.media.streaming/PlaySpeed"
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
 - PlaySpeed
targetos: Windows
req.typenames: PlaySpeed
req.redist: 
ms.custom: 19H1
---

# PlaySpeed structure


## -description


Represents a playback speed as a rational number.  


## -struct-fields




### -field streaming.PlaySpeed.Numerator

 


### -field streaming.PlaySpeed.Denominator

 




#### - Denominator

The <b>Numerator</b> should be divided by this value to obtain the play speed.  A value of 0 is not allowed.


#### - Numerator

A value that when divided by the <b>Denominator</b> represents the play speed.


## -remarks



The <b>Numerator</b> is a signed integer, allowing for negative speeds.  A negative speed means that the content is played in reverse.  A speed of 1 means that the content is played at its normal playback speed.



