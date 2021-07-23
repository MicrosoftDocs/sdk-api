---
UID: NN:evr.IMFVideoDisplayControl
title: IMFVideoDisplayControl (evr.h)
description: Controls how the Enhanced Video Renderer (EVR) displays video.
helpviewer_keywords: ["IMFVideoDisplayControl","IMFVideoDisplayControl interface [Media Foundation]","IMFVideoDisplayControl interface [Media Foundation]","described","db9b4663-9240-484f-8c47-cb1f5daa238d","evr/IMFVideoDisplayControl","mf.imfvideodisplaycontrol"]
old-location: mf\imfvideodisplaycontrol.htm
tech.root: mf
ms.assetid: db9b4663-9240-484f-8c47-cb1f5daa238d
ms.date: 12/05/2018
ms.keywords: IMFVideoDisplayControl, IMFVideoDisplayControl interface [Media Foundation], IMFVideoDisplayControl interface [Media Foundation],described, db9b4663-9240-484f-8c47-cb1f5daa238d, evr/IMFVideoDisplayControl, mf.imfvideodisplaycontrol
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
 - IMFVideoDisplayControl
 - evr/IMFVideoDisplayControl
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
 - IMFVideoDisplayControl
---

# IMFVideoDisplayControl interface


## -description

Controls how the <a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR) displays video.

The EVR presenter implements this interface. To get a pointer to the interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service identifier is GUID MR_VIDEO_RENDER_SERVICE. Call <b>GetService</b> on any of the following objects:
<ul>
<li>The <a href="/windows/desktop/medfound/media-session">Media Session</a>, if the topology contains an instance of the EVR.
            </li>
<li>The EVR media sink.
            </li>
<li>The DirectShow EVR filter.
            </li>
<li>The EVR presenter.
            </li>
</ul>If you implement a custom presenter for the EVR, the presenter can optionally expose this interface as a service.

## -inheritance

The <b>IMFVideoDisplayControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoDisplayControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/how-to-play-unprotected-media-files">How to Play Media Files with Media Foundation</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>
