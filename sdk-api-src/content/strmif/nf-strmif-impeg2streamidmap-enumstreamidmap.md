---
UID: NF:strmif.IMPEG2StreamIdMap.EnumStreamIdMap
title: IMPEG2StreamIdMap::EnumStreamIdMap (strmif.h)
description: The EnumStreamIdMap method returns a collection of all the mapped Stream IDs on this pin.
helpviewer_keywords: ["EnumStreamIdMap","EnumStreamIdMap method [DirectShow]","EnumStreamIdMap method [DirectShow]","IMPEG2StreamIdMap interface","IMPEG2StreamIdMap interface [DirectShow]","EnumStreamIdMap method","IMPEG2StreamIdMap.EnumStreamIdMap","IMPEG2StreamIdMap::EnumStreamIdMap","IMPEG2StreamIdMapEnumStreamIdMap","dshow.impeg2streamidmap_enumstreamidmap","strmif/IMPEG2StreamIdMap::EnumStreamIdMap"]
old-location: dshow\impeg2streamidmap_enumstreamidmap.htm
tech.root: dshow
ms.assetid: 2c42f042-c9fb-4cb9-90bb-4050a61b18da
ms.date: 4/26/2023
ms.keywords: EnumStreamIdMap, EnumStreamIdMap method [DirectShow], EnumStreamIdMap method [DirectShow],IMPEG2StreamIdMap interface, IMPEG2StreamIdMap interface [DirectShow],EnumStreamIdMap method, IMPEG2StreamIdMap.EnumStreamIdMap, IMPEG2StreamIdMap::EnumStreamIdMap, IMPEG2StreamIdMapEnumStreamIdMap, dshow.impeg2streamidmap_enumstreamidmap, strmif/IMPEG2StreamIdMap::EnumStreamIdMap
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMPEG2StreamIdMap::EnumStreamIdMap
 - strmif/IMPEG2StreamIdMap::EnumStreamIdMap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMPEG2StreamIdMap.EnumStreamIdMap
---

# IMPEG2StreamIdMap::EnumStreamIdMap


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>EnumStreamIdMap</code> method returns a collection of all the mapped Stream IDs on this pin.

## -parameters

### -param ppIEnumStreamIdMap [in]

<a href="/windows/desktop/api/strmif/nn-strmif-ienumstreamidmap">IEnumStreamIdMap</a> interface pointer that will be set to the returned collection.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -remarks

Currently, there is only one stream ID mapped to a given pin, therefore this collection will contain a single item.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-impeg2streamidmap">IMPEG2StreamIdMap Interface</a>