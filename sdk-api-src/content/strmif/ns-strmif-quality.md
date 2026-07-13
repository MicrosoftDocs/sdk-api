---
UID: NS:strmif.tagQuality
title: Quality (strmif.h)
description: The Quality structure describes a quality message by indicating Flood or Famine in the renderer and specifying the percentage of frames to drop or add to optimize the renderer's performance.
helpviewer_keywords: ["Quality","Quality structure [DirectShow]","QualityStructure","dshow.quality","strmif/Quality"]
old-location: dshow\quality.htm
tech.root: dshow
ms.assetid: 2ab7fcde-0e44-4d60-acf5-3638efbe15f7
ms.date: 4/26/2023
ms.keywords: Quality, Quality structure [DirectShow], QualityStructure, dshow.quality, strmif/Quality
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
req.typenames: Quality
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagQuality
 - strmif/tagQuality
 - Quality
 - strmif/Quality
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
 - Quality
---

# Quality structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Quality</code> structure describes a quality message by indicating Flood or Famine in the renderer and specifying the percentage of frames to drop or add to optimize the renderer's performance.

## -struct-fields

### -field Type

Value from the [QualityMessageType](/windows/desktop/api/strmif/ne-strmif-qualitymessagetype) enumeration, indicating whether the downstream filter needs more or less data.

### -field Proportion

Value that specifies the rate at which DirectShow should continue to send media samples. The base value is 1000, which indicates there should be no change. A percentage increase or decrease from 1000 indicates the percentage of frames to add or drop. If this value is 800, for example, DirectShow will drop 20 percent of the incoming frames to match the renderer's speed.

### -field Late

If a famine exists downstream, this is the amount of time by which the stream is lagging.

### -field TimeStamp

Value that specifies the time when DirectShow created this structure, which is usually the start time on a video sample.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>