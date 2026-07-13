---
UID: NS:dvdmedia._AM_DVD_YUV
title: AM_DVD_YUV (dvdmedia.h)
description: Contains DVD YUV subpicture data.
helpviewer_keywords: ["*PAM_DVD_YUV","AM_DVD_YUV","AM_DVD_YUV structure [DirectShow]","PAM_DVD_YUV","PAM_DVD_YUV structure pointer [DirectShow]","dshow.am_dvd_yuv","dvdmedia/AM_DVD_YUV","dvdmedia/PAM_DVD_YUV"]
old-location: dshow\am_dvd_yuv.htm
tech.root: dshow
ms.assetid: fb954bc2-4ef1-4a5f-b795-a3b2a8aae8d4
ms.date: 4/26/2023
ms.keywords: '*PAM_DVD_YUV, AM_DVD_YUV, AM_DVD_YUV structure [DirectShow], PAM_DVD_YUV, PAM_DVD_YUV structure pointer [DirectShow], dshow.am_dvd_yuv, dvdmedia/AM_DVD_YUV, dvdmedia/PAM_DVD_YUV'
req.header: dvdmedia.h
req.include-header: 
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
req.typenames: AM_DVD_YUV, *PAM_DVD_YUV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_DVD_YUV
 - dvdmedia/_AM_DVD_YUV
 - PAM_DVD_YUV
 - dvdmedia/PAM_DVD_YUV
 - AM_DVD_YUV
 - dvdmedia/AM_DVD_YUV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_DVD_YUV
---

# AM_DVD_YUV structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Contains DVD YUV subpicture data.

## -struct-fields

### -field Reserved

Reserved.

### -field Y

Y color data.

### -field U

U color data.

### -field V

V color data.

## -remarks

This structure is contained within the <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_property_sppal">AM_PROPERTY_SPPAL</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-subpicture-property-set">DVD Subpicture Property Set</a>