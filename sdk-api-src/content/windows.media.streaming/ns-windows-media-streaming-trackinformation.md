---
UID: NS:windows.media.streaming.TrackInformation
title: TrackInformation (windows.media.streaming.h)
author: windows-sdk-content
description: Contains the current track number and duration as part of the PositionInformation obtained from the DMR.
old-location: mediastreaming\trackinformation.htm
tech.root: mediastreaming
ms.assetid: 47398d9f-9462-49c1-a02c-985212a07363
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TrackInformation, TrackInformation structure [Media Streaming API], mediastreaming.trackinformation, windows/TrackInformation
ms.topic: struct
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
 - TrackInformation
product: Windows
targetos: Windows
req.typenames: TrackInformation
req.redist: 
---

# TrackInformation structure


## -description


Contains the current track number and duration as part of the <a href="https://msdn.microsoft.com/9601c1ae-3fd2-4761-8aa7-102b72ef4733">PositionInformation</a> obtained from the DMR.


## -struct-fields




### -field streaming.TrackInformation.Track

 


### -field streaming.TrackInformation.TrackId

 


### -field streaming.TrackInformation.TrackDuration

 




#### - Track

The current track number as reported by DMR.  If the DMR does not have a concept of track numbers, this value will be 0.


#### - TrackDuration

The duration of the current track.

