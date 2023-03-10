---
UID: NN:strmif.IAMVideoDecimationProperties
title: IAMVideoDecimationProperties (strmif.h)
description: The IAMVideoDecimationProperties interface controls how the Overlay Mixer performs video decimationIf a video window is smaller than the native size of the video being displayed, the video renderer must decimate the incoming video�that is, scale the video down to the smaller size. Decimation can be performed in one of the following places.The overlay hardware on the VGA chip.The scaler built in to the video port (if the connection is through a video port).The decoder supplying video to the renderer.An application can call methods on this interface to select a particular decimation strategy, in order to optimize performance. However, most applications will have no occasion to use this interface. Unless your application is designed to support particular hardware, there is no reason to modify the Overlay Mixer filter's default behavior for decimation.
helpviewer_keywords: ["IAMVideoDecimationProperties","IAMVideoDecimationProperties interface [DirectShow]","IAMVideoDecimationProperties interface [DirectShow]","described","IAMVideoDecimationPropertiesInterface","dshow.iamvideodecimationproperties","strmif/IAMVideoDecimationProperties"]
old-location: dshow\iamvideodecimationproperties.htm
tech.root: dshow
ms.assetid: fd435eff-a4bc-40b3-8aa7-50d78d17e4ce
ms.date: 12/05/2018
ms.keywords: IAMVideoDecimationProperties, IAMVideoDecimationProperties interface [DirectShow], IAMVideoDecimationProperties interface [DirectShow],described, IAMVideoDecimationPropertiesInterface, dshow.iamvideodecimationproperties, strmif/IAMVideoDecimationProperties
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
 - IAMVideoDecimationProperties
 - strmif/IAMVideoDecimationProperties
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
 - IAMVideoDecimationProperties
---

# IAMVideoDecimationProperties interface


## -description

The <code>IAMVideoDecimationProperties</code> interface controls how the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> performs video decimation

If a video window is smaller than the native size of the video being displayed, the video renderer must <i>decimate</i> the incoming video—that is, scale the video down to the smaller size. Decimation can be performed in one of the following places.

<ul>
<li>The overlay hardware on the VGA chip.</li>
<li>The scaler built in to the video port (if the connection is through a video port).</li>
<li>The decoder supplying video to the renderer.</li>
</ul>
An application can call methods on this interface to select a particular decimation strategy, in order to optimize performance. However, most applications will have no occasion to use this interface. Unless your application is designed to support particular hardware, there is no reason to modify the Overlay Mixer filter's default behavior for decimation.

## -inheritance

The <b>IAMVideoDecimationProperties</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVideoDecimationProperties</b> also has these types of members:

