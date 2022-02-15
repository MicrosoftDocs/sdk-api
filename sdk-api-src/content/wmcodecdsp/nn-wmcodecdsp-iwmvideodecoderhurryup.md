---
UID: NN:wmcodecdsp.IWMVideoDecoderHurryup
title: IWMVideoDecoderHurryup (wmcodecdsp.h)
description: Controls the speed of the video decoder.
helpviewer_keywords: ["IWMVideoDecoderHurryup","IWMVideoDecoderHurryup interface [Media Foundation]","IWMVideoDecoderHurryup interface [Media Foundation]","described","codecapi.iwmvideodecoderhurryupinterface","mf.iwmvideodecoderhurryup","mf.iwmvideodecoderhurryupinterface","wmcodecdsp/IWMVideoDecoderHurryup"]
old-location: mf\iwmvideodecoderhurryupinterface.htm
tech.root: mf
ms.assetid: 5e33be5f-5ce8-4f4f-94db-4be2dfcaeec0
ms.date: 12/05/2018
ms.keywords: IWMVideoDecoderHurryup, IWMVideoDecoderHurryup interface [Media Foundation], IWMVideoDecoderHurryup interface [Media Foundation],described, codecapi.iwmvideodecoderhurryupinterface, mf.iwmvideodecoderhurryup, mf.iwmvideodecoderhurryupinterface, wmcodecdsp/IWMVideoDecoderHurryup
req.header: wmcodecdsp.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMVideoDecoderHurryup
 - wmcodecdsp/IWMVideoDecoderHurryup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMVideoDecoderHurryup
---

# IWMVideoDecoderHurryup interface


## -description

Controls the speed of the video decoder.



This interface is implemented by the video decoder objects. You can obtain a pointer to <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderhurryup">IWMVideoDecoderHurryup</a> by calling the <b>QueryInterface</b> method of any other interface of the decoder, such as <a href="/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject</a> or <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>

## -inheritance

The <b>IWMVideoDecoderHurryup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMVideoDecoderHurryup</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
