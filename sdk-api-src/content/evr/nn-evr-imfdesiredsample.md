---
UID: NN:evr.IMFDesiredSample
title: IMFDesiredSample (evr.h)
description: Enables the presenter for the enhanced video renderer (EVR) to request a specific frame from the video mixer.
helpviewer_keywords: ["373c076c-6329-4332-9f07-f18a01197659","IMFDesiredSample","IMFDesiredSample interface [Media Foundation]","IMFDesiredSample interface [Media Foundation]","described","evr/IMFDesiredSample","mf.imfdesiredsample"]
old-location: mf\imfdesiredsample.htm
tech.root: mfarchive
ms.assetid: 373c076c-6329-4332-9f07-f18a01197659
ms.date: 12/05/2018
ms.keywords: 373c076c-6329-4332-9f07-f18a01197659, IMFDesiredSample, IMFDesiredSample interface [Media Foundation], IMFDesiredSample interface [Media Foundation],described, evr/IMFDesiredSample, mf.imfdesiredsample
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFDesiredSample
 - evr/IMFDesiredSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFDesiredSample
archived: true
---

# IMFDesiredSample interface


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Enables the presenter for the enhanced video renderer (EVR) to request a specific frame from the video mixer.

The sample objects created by the <a href="/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface">MFCreateVideoSampleFromSurface</a> function implement this interface. To retrieve a pointer to this interface, call <b>QueryInterface</b> on the sample.

## -inheritance

The <b>IMFDesiredSample</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFDesiredSample</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
