---
UID: NN:evr.IMFVideoPositionMapper
title: IMFVideoPositionMapper (evr.h)
description: Maps a position on an input video stream to the corresponding position on an output video stream.
helpviewer_keywords: ["282fa124-909f-49dc-9a86-3d962193e903","IMFVideoPositionMapper","IMFVideoPositionMapper interface [Media Foundation]","IMFVideoPositionMapper interface [Media Foundation]","described","evr/IMFVideoPositionMapper","mf.imfvideopositionmapper"]
old-location: mf\imfvideopositionmapper.htm
tech.root: mfarchive
ms.assetid: 282fa124-909f-49dc-9a86-3d962193e903
ms.date: 12/05/2018
ms.keywords: 282fa124-909f-49dc-9a86-3d962193e903, IMFVideoPositionMapper, IMFVideoPositionMapper interface [Media Foundation], IMFVideoPositionMapper interface [Media Foundation],described, evr/IMFVideoPositionMapper, mf.imfvideopositionmapper
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFVideoPositionMapper
 - evr/IMFVideoPositionMapper
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoPositionMapper
archived: true
---

# IMFVideoPositionMapper interface


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Maps a position on an input video stream to the corresponding position on an output video stream.

To obtain a pointer to this interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> on the renderer with the service GUID MR_VIDEO_RENDER_SERVICE.

## -inheritance

The <b>IMFVideoPositionMapper</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoPositionMapper</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
