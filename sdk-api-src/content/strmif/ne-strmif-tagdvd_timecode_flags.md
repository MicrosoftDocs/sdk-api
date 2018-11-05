---
UID: NE:strmif.tagDVD_TIMECODE_FLAGS
title: tagDVD_TIMECODE_FLAGS
author: windows-sdk-content
description: Indicates the frame rate at which a DVD has been authored to play.
old-location: dshow\dvd_timecode_flags.htm
tech.root: DirectShow
ms.assetid: 2dc5ce97-12a4-43a0-b897-14fea32d8efc
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DVD_TC_FLAG_25fps, DVD_TC_FLAG_30fps, DVD_TC_FLAG_DropFrame, DVD_TC_FLAG_Interpolated, DVD_TIMECODE_FLAGS, DVD_TIMECODE_FLAGS , DVD_TIMECODE_FLAGS enumeration [DirectShow], DVD_TIMECODE_FLAGSEnumeration, dshow.dvd_timecode_flags, strmif/DVD_TC_FLAG_25fps, strmif/DVD_TC_FLAG_30fps, strmif/DVD_TC_FLAG_DropFrame, strmif/DVD_TC_FLAG_Interpolated, strmif/DVD_TIMECODE_FLAGS, tagDVD_TIMECODE_FLAGS
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_TIMECODE_FLAGS
product: Windows
targetos: Windows
req.typenames: DVD_TIMECODE_FLAGS
req.redist: 
---

# tagDVD_TIMECODE_FLAGS enumeration


## -description



Indicates the frame rate at which a DVD has been authored to play.




## -enum-fields




### -field DVD_TC_FLAG_25fps

Disc is authored to play at 25 frames per second.


### -field DVD_TC_FLAG_30fps

Disc is authored to play at 30 frames per second.


### -field DVD_TC_FLAG_DropFrame

Disc is authored to play at 29.97 frames per second.


### -field DVD_TC_FLAG_Interpolated

Value representing the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator Filter</a> filter's best estimate of the disc's frame rate.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/90768da1-592a-49ec-99b0-56f463c322e8">IDvdInfo2::GetTotalTitleTime</a>
 

 

