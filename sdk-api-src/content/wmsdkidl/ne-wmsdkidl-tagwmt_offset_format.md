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

# tagWMT_OFFSET_FORMAT enumeration


## -description



The <b>WMT_OFFSET_FORMAT</b> enumeration type defines the types of offsets used in this SDK.




## -enum-fields




### -field WMT_OFFSET_FORMAT_100NS

An offset into a file is specified by presentation time in 100-nanosecond units.


### -field WMT_OFFSET_FORMAT_FRAME_NUMBERS

An offset into a file is specified by frame number.


### -field WMT_OFFSET_FORMAT_PLAYLIST_OFFSET

An offset of playlist entries.


### -field WMT_OFFSET_FORMAT_TIMECODE

An offset into a file is specified by presentation time as identified by SMTPE time codes.


### -field WMT_OFFSET_FORMAT_100NS_APPROXIMATE

Used to specify approximate seeking. This type of offset seeks to the closest key frame prior to the time specified.


## -remarks



<b>WMT_OFFSET_FORMAT</b> is used as an input parameter to <a href="https://msdn.microsoft.com/64b922be-3a8f-4cbe-aa1d-aa3833e1f0fa">IWMReaderAdvanced3::StartAtPosition</a>. The value passed specifies whether the reader should begin playback at a specified presentation time, frame number, or offset into a playlist.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

