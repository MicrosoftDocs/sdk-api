---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# AM_SEEKING_SeekingCapabilities enumeration


## -description



Specifies the seeking capabilities of a media stream.




## -enum-fields




### -field AM_SEEKING_CanSeekAbsolute


            The stream can seek to an absolute position.
          


### -field AM_SEEKING_CanSeekForwards


            The stream can seek forward.
          


### -field AM_SEEKING_CanSeekBackwards


            The stream can seek backward.
          


### -field AM_SEEKING_CanGetCurrentPos


            The stream can report its current position. See Remarks.
          


### -field AM_SEEKING_CanGetStopPos


            The stream can report its stop position.
          


### -field AM_SEEKING_CanGetDuration


            The stream can report its duration.
          


### -field AM_SEEKING_CanPlayBackwards


            The stream can play backward.
          


### -field AM_SEEKING_CanDoSegments


            The stream can do seamless looping (see <a href="https://msdn.microsoft.com/aa1369fd-a57a-4246-bb23-969f6ce3cad8">IMediaSeeking::SetPositions</a>).
          


### -field AM_SEEKING_Source


            Reserved.
          


## -remarks



Most DirectShow filters do not report the <b>AM_SEEKING_CanGetCurrentPos</b> capability flag. However, the Filter Graph Manager's implementation of <a href="https://msdn.microsoft.com/4dca0c9e-ce95-4716-8e4d-ce8bf83628d6">IMediaSeeking::GetCurrentPosition</a> is based on the reference clock, so you can call this method even if the capabilities flags do not include <b>AM_SEEKING_CanGetCurrentPos</b>.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/d0062f66-213d-4f91-9f73-780be39ee432">IMediaSeeking::CheckCapabilities</a>



<a href="https://msdn.microsoft.com/84dd3c21-9c72-4433-bd03-29520dc138ca">IMediaSeeking::GetCapabilities</a>
 

 

