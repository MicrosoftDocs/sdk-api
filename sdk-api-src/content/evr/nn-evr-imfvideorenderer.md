---
UID: NN:evr.IMFVideoRenderer
title: IMFVideoRenderer (evr.h)
description: Sets a new mixer or presenter for the Enhanced Video Renderer (EVR).
helpviewer_keywords: ["70596630-5131-460f-9cb3-adcea201c3b2","IMFVideoRenderer","IMFVideoRenderer interface [Media Foundation]","IMFVideoRenderer interface [Media Foundation]","described","evr/IMFVideoRenderer","mf.imfvideorenderer"]
old-location: mf\imfvideorenderer.htm
tech.root: mf
ms.assetid: 70596630-5131-460f-9cb3-adcea201c3b2
ms.date: 12/05/2018
ms.keywords: 70596630-5131-460f-9cb3-adcea201c3b2, IMFVideoRenderer, IMFVideoRenderer interface [Media Foundation], IMFVideoRenderer interface [Media Foundation],described, evr/IMFVideoRenderer, mf.imfvideorenderer
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
 - IMFVideoRenderer
 - evr/IMFVideoRenderer
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
 - IMFVideoRenderer
---

# IMFVideoRenderer interface


## -description

Sets a new mixer or presenter for the <a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR).

Both the EVR media sink and the DirectShow EVR filter implement this interface. To get a pointer to the interface, call <b>QueryInterface</b> on the media sink or the filter. Do not use <a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice">IMFGetService</a> to get a pointer to this interface.

## -inheritance

The <b>IMFVideoRenderer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoRenderer</b> also has these types of members:

## -remarks

The EVR activation object returned by the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate">MFCreateVideoRendererActivate</a> function does not expose this interface. Instead, the activation object supports attributes that specify a custom mixer or presenter. For more information, see <a href="/windows/desktop/medfound/enhanced-video-renderer-attributes">Enhanced Video Renderer Attributes</a>.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
