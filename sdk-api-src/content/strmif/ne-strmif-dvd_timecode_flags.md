---
UID: NE:strmif.tagDVD_TIMECODE_FLAGS
title: DVD_TIMECODE_FLAGS (strmif.h)
author: windows-sdk-content
description: Indicates the frame rate at which a DVD has been authored to play.
old-location: dshow\dvd_timecode_flags.htm
tech.root: DirectShow
ms.assetid: 2dc5ce97-12a4-43a0-b897-14fea32d8efc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DVD_TC_FLAG_25fps, DVD_TC_FLAG_30fps, DVD_TC_FLAG_DropFrame, DVD_TC_FLAG_Interpolated, DVD_TIMECODE_FLAGS, DVD_TIMECODE_FLAGS , DVD_TIMECODE_FLAGS enumeration [DirectShow], DVD_TIMECODE_FLAGSEnumeration, dshow.dvd_timecode_flags, strmif/DVD_TC_FLAG_25fps, strmif/DVD_TC_FLAG_30fps, strmif/DVD_TC_FLAG_DropFrame, strmif/DVD_TC_FLAG_Interpolated, strmif/DVD_TIMECODE_FLAGS
ms.topic: enum
f1_keywords: 
 - "strmif/DVD_TIMECODE_FLAGS"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: DVD_TIMECODE_FLAGS
req.redist: 
ms.custom: 19H1
---

# DVD_TIMECODE_FLAGS enumeration


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

Value representing the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator Filter</a> filter's best estimate of the disc's frame rate.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-gettotaltitletime">IDvdInfo2::GetTotalTitleTime</a>
 

 

