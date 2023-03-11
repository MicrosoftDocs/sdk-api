---
UID: NE:strmif.tagDVD_TIMECODE_FLAGS
title: DVD_TIMECODE_FLAGS (strmif.h)
description: Indicates the frame rate at which a DVD has been authored to play.
helpviewer_keywords: ["DVD_TC_FLAG_25fps","DVD_TC_FLAG_30fps","DVD_TC_FLAG_DropFrame","DVD_TC_FLAG_Interpolated","DVD_TIMECODE_FLAGS","DVD_TIMECODE_FLAGS","DVD_TIMECODE_FLAGS enumeration [DirectShow]","DVD_TIMECODE_FLAGSEnumeration","dshow.dvd_timecode_flags","strmif/DVD_TC_FLAG_25fps","strmif/DVD_TC_FLAG_30fps","strmif/DVD_TC_FLAG_DropFrame","strmif/DVD_TC_FLAG_Interpolated","strmif/DVD_TIMECODE_FLAGS"]
old-location: dshow\dvd_timecode_flags.htm
tech.root: dshow
ms.assetid: 2dc5ce97-12a4-43a0-b897-14fea32d8efc
ms.date: 12/05/2018
ms.keywords: DVD_TC_FLAG_25fps, DVD_TC_FLAG_30fps, DVD_TC_FLAG_DropFrame, DVD_TC_FLAG_Interpolated, DVD_TIMECODE_FLAGS, DVD_TIMECODE_FLAGS , DVD_TIMECODE_FLAGS enumeration [DirectShow], DVD_TIMECODE_FLAGSEnumeration, dshow.dvd_timecode_flags, strmif/DVD_TC_FLAG_25fps, strmif/DVD_TC_FLAG_30fps, strmif/DVD_TC_FLAG_DropFrame, strmif/DVD_TC_FLAG_Interpolated, strmif/DVD_TIMECODE_FLAGS
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
targetos: Windows
req.typenames: DVD_TIMECODE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_TIMECODE_FLAGS
 - strmif/tagDVD_TIMECODE_FLAGS
 - DVD_TIMECODE_FLAGS
 - strmif/DVD_TIMECODE_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_TIMECODE_FLAGS
---

# DVD_TIMECODE_FLAGS enumeration


## -description

Indicates the frame rate at which a DVD has been authored to play.

## -enum-fields

### -field DVD_TC_FLAG_25fps:0x1

Disc is authored to play at 25 frames per second.

### -field DVD_TC_FLAG_30fps:0x2

Disc is authored to play at 30 frames per second.

### -field DVD_TC_FLAG_DropFrame:0x4

Disc is authored to play at 29.97 frames per second.

### -field DVD_TC_FLAG_Interpolated:0x8

Value representing the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator Filter</a> filter's best estimate of the disc's frame rate.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-gettotaltitletime">IDvdInfo2::GetTotalTitleTime</a>
