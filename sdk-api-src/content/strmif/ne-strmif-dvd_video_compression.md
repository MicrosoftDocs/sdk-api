---
UID: NE:strmif.tagDVD_VIDEO_COMPRESSION
title: DVD_VIDEO_COMPRESSION (strmif.h)
description: Defines the possible DVD video compression types.
helpviewer_keywords: ["DVD_VIDEO_COMPRESSION","DVD_VIDEO_COMPRESSION","DVD_VIDEO_COMPRESSION enumeration [DirectShow]","DVD_VIDEO_COMPRESSIONEnumeration","DVD_VideoCompression_MPEG1","DVD_VideoCompression_MPEG2","DVD_VideoCompression_Other","dshow.dvd_video_compression","strmif/DVD_VIDEO_COMPRESSION","strmif/DVD_VideoCompression_MPEG1","strmif/DVD_VideoCompression_MPEG2","strmif/DVD_VideoCompression_Other"]
old-location: dshow\dvd_video_compression.htm
tech.root: dshow
ms.assetid: e147a860-4c69-4da0-96d1-dfc4957880d9
ms.date: 12/05/2018
ms.keywords: DVD_VIDEO_COMPRESSION, DVD_VIDEO_COMPRESSION , DVD_VIDEO_COMPRESSION enumeration [DirectShow], DVD_VIDEO_COMPRESSIONEnumeration, DVD_VideoCompression_MPEG1, DVD_VideoCompression_MPEG2, DVD_VideoCompression_Other, dshow.dvd_video_compression, strmif/DVD_VIDEO_COMPRESSION, strmif/DVD_VideoCompression_MPEG1, strmif/DVD_VideoCompression_MPEG2, strmif/DVD_VideoCompression_Other
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
req.typenames: DVD_VIDEO_COMPRESSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_VIDEO_COMPRESSION
 - strmif/tagDVD_VIDEO_COMPRESSION
 - DVD_VIDEO_COMPRESSION
 - strmif/DVD_VIDEO_COMPRESSION
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
 - DVD_VIDEO_COMPRESSION
---

# DVD_VIDEO_COMPRESSION enumeration


## -description

Defines the possible DVD video compression types.

## -enum-fields

### -field DVD_VideoCompression_Other:0

Unrecognized compression type.

### -field DVD_VideoCompression_MPEG1:1

MPEG-1 compression type.

### -field DVD_VideoCompression_MPEG2:2

MPEG-2 compression type.

## -remarks

This enumeration is a member of the [DVD_VideoAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_videoattributes) structure, which is filled by a call to the <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentvideoattributes">IDvdInfo2::GetCurrentVideoAttributes</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
