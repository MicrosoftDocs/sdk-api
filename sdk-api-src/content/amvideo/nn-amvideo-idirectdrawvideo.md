---
UID: NN:amvideo.IDirectDrawVideo
title: IDirectDrawVideo (amvideo.h)
description: The IDirectDrawVideo interface queries the Video Renderer filter about DirectDraw surfaces and hardware capabilities.Applications can use this interface to control what DirectDraw features the Video Renderer will take advantage of.
helpviewer_keywords: ["IDirectDrawVideo","IDirectDrawVideo interface [DirectShow]","IDirectDrawVideo interface [DirectShow]","described","IDirectDrawVideoInterface","amvideo/IDirectDrawVideo","dshow.idirectdrawvideo"]
old-location: dshow\idirectdrawvideo.htm
tech.root: dshow
ms.assetid: b918bf3b-b91b-40fb-abb8-4115a4f254bb
ms.date: 4/26/2023
ms.keywords: IDirectDrawVideo, IDirectDrawVideo interface [DirectShow], IDirectDrawVideo interface [DirectShow],described, IDirectDrawVideoInterface, amvideo/IDirectDrawVideo, dshow.idirectdrawvideo
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IDirectDrawVideo
 - amvideo/IDirectDrawVideo
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
 - IDirectDrawVideo
---

# IDirectDrawVideo interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IDirectDrawVideo</code> interface queries the <a href="/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter about DirectDraw surfaces and hardware capabilities.

Applications can use this interface to control what DirectDraw features the Video Renderer will take advantage of. For example, if you are positive that you don't want the Video Renderer to use a hardware overlay you can disable its use via the <a href="/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-setswitches">SetSwitches</a> method.

<div class="alert"><b>Note</b>  You can't use this interface to force the Video Renderer to use a particular DirectDraw feature; you can only stop it from using that feature.</div>
<div> </div>
There is some duplication in this interface with the <b>IDirectDraw</b> interface; however, this interface enables simple access to that information without calling the DirectDraw provider directly.

The Video Renderer does not load DirectDraw until it is connected, and likewise DirectDraw is unloaded only when the renderer is disconnected. When the renderer has allocated the DirectDraw surfaces it will use for video playback, an application can obtain a <b>DDSURFACEDESC</b> structure describing it. By passing in a pointer to a <b>DDSURFACEDESC</b> structure, the renderer will fill in the structure with the details of the current surface. If DirectDraw has not been loaded, the renderer will return E_FAIL. If the renderer is using DCI (the predecessor to DirectDraw), the <b>DDSURFACEDESC</b> structure is not filled in but the call will return S_FALSE. The only type of DCI surfaces the renderer uses are primary surfaces.

## -inheritance

The <b>IDirectDrawVideo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDrawVideo</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

