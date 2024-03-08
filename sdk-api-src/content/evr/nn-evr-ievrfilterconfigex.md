---
UID: NN:evr.IEVRFilterConfigEx
title: IEVRFilterConfigEx (evr.h)
description: Configures the DirectShow Enhanced Video Renderer (EVR) filter.
helpviewer_keywords: ["IEVRFilterConfigEx","IEVRFilterConfigEx interface [Media Foundation]","IEVRFilterConfigEx interface [Media Foundation]","described","evr/IEVRFilterConfigEx","mf.ievrfilterconfigex"]
old-location: mf\ievrfilterconfigex.htm
tech.root: mfarchive
ms.assetid: bbe85dc1-af9c-4be7-9064-d61bba160942
ms.date: 12/05/2018
ms.keywords: IEVRFilterConfigEx, IEVRFilterConfigEx interface [Media Foundation], IEVRFilterConfigEx interface [Media Foundation],described, evr/IEVRFilterConfigEx, mf.ievrfilterconfigex
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEVRFilterConfigEx
 - evr/IEVRFilterConfigEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - evr.h
api_name:
 - IEVRFilterConfigEx
archived: true
---

# IEVRFilterConfigEx interface


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Configures the DirectShow <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer</a> (EVR) filter.  To get a pointer to this interface, call <b>QueryInterface</b> on the  EVR filter.

## -inheritance

The <b>IEVRFilterConfigEx</b> interface inherits from <a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig">IEVRFilterConfig</a>. <b>IEVRFilterConfigEx</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer Filter</a>



<a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig">IEVRFilterConfig</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/video-quality-management">Video Quality Management</a>
