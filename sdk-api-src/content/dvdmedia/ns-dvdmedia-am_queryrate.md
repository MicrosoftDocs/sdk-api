---
UID: NS:dvdmedia.AM_QueryRate
title: AM_QueryRate (dvdmedia.h)
description: The AM_QueryRate structure is used to query the decoder's maximum full-frame rate for forward and reverse playback.
helpviewer_keywords: ["AM_QueryRate","AM_QueryRate structure [DirectShow]","AM_QueryRateStructure","dshow.am_queryrate","dvdmedia/AM_QueryRate"]
old-location: dshow\am_queryrate.htm
tech.root: dshow
ms.assetid: a791f6ac-f415-4641-bac1-26db983a1ef7
ms.date: 4/26/2023
ms.keywords: AM_QueryRate, AM_QueryRate structure [DirectShow], AM_QueryRateStructure, dshow.am_queryrate, dvdmedia/AM_QueryRate
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
req.typenames: AM_QueryRate
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AM_QueryRate
 - dvdmedia/AM_QueryRate
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
 - AM_QueryRate
---

# AM_QueryRate structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AM_QueryRate</b> structure is used to query the decoder's maximum full-frame rate for forward and reverse playback.

## -struct-fields

### -field lMaxForwardFullFrame

Specifies the maximum forward full-frame rate, as rate x 10000.

### -field lMaxReverseFullFrame

Specifies the maximum reverse full-frame rate, as rate x 10000.

## -remarks

Rate is the inverse of speed. For example, if the playback speed is 2x, the rate is 1/2, so the <b>Rate</b> member is set to 5000. Reverse rates are negative.

## -see-also

<a href="/windows/desktop/DirectShow/am-rate-queryfullframerate-property">AM_RATE_QueryFullFrameRate Property</a>



<a href="/windows/desktop/DirectShow/rate-change-property-set">Rate Change Property Set</a>

