---
UID: NE:strmif.AM_SEEKING_SeekingCapabilities
title: AM_SEEKING_SeekingCapabilities
author: windows-sdk-content
description: Specifies the seeking capabilities of a media stream.
old-location: dshow\am_seeking_seeking_capabilities.htm
old-project: DirectShow
ms.assetid: 1c7ad11b-2d10-409e-a292-b777566c637d
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: AM_SEEKING_CanDoSegments, AM_SEEKING_CanGetCurrentPos, AM_SEEKING_CanGetDuration, AM_SEEKING_CanGetStopPos, AM_SEEKING_CanPlayBackwards, AM_SEEKING_CanSeekAbsolute, AM_SEEKING_CanSeekBackwards, AM_SEEKING_CanSeekForwards, AM_SEEKING_SEEKING_CAPABILITIES, AM_SEEKING_SEEKING_CAPABILITIES , AM_SEEKING_SEEKING_CAPABILITIES enumeration [DirectShow], AM_SEEKING_SEEKING_CAPABILITIESEnumeration, AM_SEEKING_SeekingCapabilities, AM_SEEKING_Source, dshow.am_seeking_seeking_capabilities, strmif/AM_SEEKING_CanDoSegments, strmif/AM_SEEKING_CanGetCurrentPos, strmif/AM_SEEKING_CanGetDuration, strmif/AM_SEEKING_CanGetStopPos, strmif/AM_SEEKING_CanPlayBackwards, strmif/AM_SEEKING_CanSeekAbsolute, strmif/AM_SEEKING_CanSeekBackwards, strmif/AM_SEEKING_CanSeekForwards, strmif/AM_SEEKING_SEEKING_CAPABILITIES, strmif/AM_SEEKING_Source
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
tech.root: 
req.typenames: AM_SEEKING_SEEKING_CAPABILITIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - AM_SEEKING_SEEKING_CAPABILITIES
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Outlook Express 6.0
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
 

 

