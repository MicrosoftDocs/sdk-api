---
UID: NS:dvdmedia._AM_PROPERTY_SPPAL
title: AM_PROPERTY_SPPAL (dvdmedia.h)
description: Specifies the DVD subpicture palette.
helpviewer_keywords: ["*PAM_PROPERTY_SPPAL","AM_PROPERTY_SPPAL","AM_PROPERTY_SPPAL structure [DirectShow]","PAM_PROPERTY_SPPAL","PAM_PROPERTY_SPPAL structure pointer [DirectShow]","dshow.am_property_sppal","dvdmedia/AM_PROPERTY_SPPAL","dvdmedia/PAM_PROPERTY_SPPAL"]
old-location: dshow\am_property_sppal.htm
tech.root: dshow
ms.assetid: ac368cbe-aaf6-42d5-a8bd-3652800af640
ms.date: 4/26/2023
ms.keywords: '*PAM_PROPERTY_SPPAL, AM_PROPERTY_SPPAL, AM_PROPERTY_SPPAL structure [DirectShow], PAM_PROPERTY_SPPAL, PAM_PROPERTY_SPPAL structure pointer [DirectShow], dshow.am_property_sppal, dvdmedia/AM_PROPERTY_SPPAL, dvdmedia/PAM_PROPERTY_SPPAL'
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
req.typenames: AM_PROPERTY_SPPAL, *PAM_PROPERTY_SPPAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_PROPERTY_SPPAL
 - dvdmedia/_AM_PROPERTY_SPPAL
 - PAM_PROPERTY_SPPAL
 - dvdmedia/PAM_PROPERTY_SPPAL
 - AM_PROPERTY_SPPAL
 - dvdmedia/AM_PROPERTY_SPPAL
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
 - AM_PROPERTY_SPPAL
---

# AM_PROPERTY_SPPAL structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the DVD subpicture palette.

## -struct-fields

### -field sppal

Array of 16 YUV elements that correspond to the 4-bit color numbers requested within the subpicture command stream. The YUV elements are of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvd_yuv">AM_DVD_YUV</a>.

## -remarks

The AM_PROPERTY_DVDSUBPIC_PALETTE property uses this structure.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-subpicture-property-set">DVD Subpicture Property Set</a>