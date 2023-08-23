---
UID: NS:strmif.tagCOLORKEY
title: COLORKEY (strmif.h)
description: The COLORKEY structure communicates color key information between the renderer and another filter.
helpviewer_keywords: ["COLORKEY","COLORKEY structure [DirectShow]","COLORKEYStructure","dshow.colorkey","strmif/COLORKEY"]
old-location: dshow\colorkey.htm
tech.root: dshow
ms.assetid: 1563488a-e4e5-472d-b665-5bbcb13fad1a
ms.date: 4/26/2023
ms.keywords: COLORKEY, COLORKEY structure [DirectShow], COLORKEYStructure, dshow.colorkey, strmif/COLORKEY
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
req.typenames: COLORKEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCOLORKEY
 - strmif/tagCOLORKEY
 - COLORKEY
 - strmif/COLORKEY
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
 - COLORKEY
---

# COLORKEY structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>COLORKEY</code> structure communicates color key information between the renderer and another filter.

## -struct-fields

### -field KeyType

Key type. Can be <b>CK_NOCOLORKEY</b>, <b>CK_INDEX</b>, or <b>CK_RGB</b>. The <b>CK_INDEX</b> and <b>CK_RGB</b> can be combined with a bitwise <b>OR</b>.

### -field PaletteIndex

Palette index.

### -field LowColorValue

Lowest RGB color value.

### -field HighColorValue

Highest RGB color value.

## -remarks

The video renderer supports a data transport accessed through the <a href="/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay</a> interface. This will typically be used by hardware decoder filters that need the renderer to communicate where to put the data rather than requiring the renderer to draw the data. One mechanism for communicating where to put the images is by using a color key. This structure is used by a filter (typically a hardware decoder) to describe color key requirements to the video renderer.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>