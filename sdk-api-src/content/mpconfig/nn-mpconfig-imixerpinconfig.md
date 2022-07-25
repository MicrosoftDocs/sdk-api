---
UID: NN:mpconfig.IMixerPinConfig
title: IMixerPinConfig (mpconfig.h)
description: The IMixerPinConfig interface is exposed on the input pins of the Overlay Mixer filter and contains methods that manipulate video streams in various ways.
helpviewer_keywords: ["IMixerPinConfig","IMixerPinConfig interface [DirectShow]","IMixerPinConfig interface [DirectShow]","described","IMixerPinConfigInterface","dshow.imixerpinconfig","mpconfig/IMixerPinConfig"]
old-location: dshow\imixerpinconfig.htm
tech.root: dshow
ms.assetid: 6a4f3462-4596-4f02-a41f-47161f8aa4db
ms.date: 12/05/2018
ms.keywords: IMixerPinConfig, IMixerPinConfig interface [DirectShow], IMixerPinConfig interface [DirectShow],described, IMixerPinConfigInterface, dshow.imixerpinconfig, mpconfig/IMixerPinConfig
req.header: mpconfig.h
req.include-header: 
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
 - IMixerPinConfig
 - mpconfig/IMixerPinConfig
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
 - IMixerPinConfig
---

# IMixerPinConfig interface


## -description

The <code>IMixerPinConfig</code> interface is exposed on the input pins of the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter and contains methods that manipulate video streams in various ways. The Overlay Mixer contains multiple input pins that are dynamically created as video input streams are added. The video stream on the first pin is known as the <i>primary stream</i> and subsequent streams are known as <i>secondary streams</i>.

Use this interface to manipulate the parameters involved in mixing various video streams. These parameters include getting and setting position, z-order, blending and transparency levels, aspect ratio correction, and color keys of streams.

When setting the position of video streams in the display window, the default relative position of all secondary streams is {0, 0, 0, 0}. Therefore, use the <a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setrelativeposition">IMixerPinConfig::SetRelativePosition</a> method on secondary streams to ensure that all video streams are placed properly.

Applications use this interface to get and set attributes when mixing multiple video streams.

## -inheritance

The <b>IMixerPinConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMixerPinConfig</b> also has these types of members:

