---
UID: NN:videoacc.IAMVideoAccelerator
title: IAMVideoAccelerator (videoacc.h)
description: The IAMVideoAccelerator interface enables a video decoder filter to access DirectX Video Acceleration (DXVA) 1.0 functionality.
helpviewer_keywords: ["IAMVideoAccelerator","IAMVideoAccelerator interface [DirectShow]","IAMVideoAccelerator interface [DirectShow]","described","IAMVideoAcceleratorInterface","dshow.iamvideoaccelerator","videoacc/IAMVideoAccelerator"]
old-location: dshow\iamvideoaccelerator.htm
tech.root: dshow
ms.assetid: 78e0a165-5a19-4dca-8d6c-445345772824
ms.date: 12/05/2018
ms.keywords: IAMVideoAccelerator, IAMVideoAccelerator interface [DirectShow], IAMVideoAccelerator interface [DirectShow],described, IAMVideoAcceleratorInterface, dshow.iamvideoaccelerator, videoacc/IAMVideoAccelerator
req.header: videoacc.h
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
 - IAMVideoAccelerator
 - videoacc/IAMVideoAccelerator
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
 - IAMVideoAccelerator
---

# IAMVideoAccelerator interface


## -description

The <b>IAMVideoAccelerator</b> interface enables a video decoder filter to access DirectX Video Acceleration (DXVA) 1.0 functionality. Applications should not call methods on this interface.

The Video Mixing Renderer filter's input pins support this interface, and so does pin 0 on the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>. If a video decoder filter calls methods on this interface, the decoder should support the <a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify">IAMVideoAcceleratorNotify</a> interface on its output pin. For more information on how to use this interface, see <a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVideoAccelerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVideoAccelerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows-hardware/drivers/display/directx-video-acceleration">DXVA 1.0 specification</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>
