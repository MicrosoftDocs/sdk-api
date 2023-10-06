---
UID: NE:strmif.tagDVD_DISC_SIDE
title: DVD_DISC_SIDE (strmif.h)
description: Indicates the sides of a DVD disc.
helpviewer_keywords: ["DVD_DISC_SIDE","DVD_DISC_SIDE","DVD_DISC_SIDE enumeration [DirectShow]","DVD_DISC_SIDEEnumeration","DVD_SIDE_A","DVD_SIDE_B","dshow.dvd_disc_side","strmif/DVD_DISC_SIDE","strmif/DVD_SIDE_A","strmif/DVD_SIDE_B"]
old-location: dshow\dvd_disc_side.htm
tech.root: dshow
ms.assetid: 50ea509c-15fc-4066-ad86-04e5e87fdfa6
ms.date: 4/26/2023
ms.keywords: DVD_DISC_SIDE, DVD_DISC_SIDE , DVD_DISC_SIDE enumeration [DirectShow], DVD_DISC_SIDEEnumeration, DVD_SIDE_A, DVD_SIDE_B, dshow.dvd_disc_side, strmif/DVD_DISC_SIDE, strmif/DVD_SIDE_A, strmif/DVD_SIDE_B
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
req.typenames: DVD_DISC_SIDE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_DISC_SIDE
 - strmif/tagDVD_DISC_SIDE
 - DVD_DISC_SIDE
 - strmif/DVD_DISC_SIDE
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
 - DVD_DISC_SIDE
---

# DVD_DISC_SIDE enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Indicates the sides of a DVD disc.

## -enum-fields

### -field DVD_SIDE_A:1

Side A.

### -field DVD_SIDE_B:2

Side B.

## -remarks

This enumeration is used in the <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdvolumeinfo">IDvdInfo2::GetDVDVolumeInfo</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdvolumeinfo">IDvdInfo2::GetDVDVolumeInfo</a>
