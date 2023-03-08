---
UID: NN:videoacc.IAMVideoAcceleratorNotify
title: IAMVideoAcceleratorNotify (videoacc.h)
description: The IAMVideoAcceleratorNotify interface is a callback interface used in conjunction with the IAMVideoAccelerator interface.
helpviewer_keywords: ["IAMVideoAcceleratorNotify","IAMVideoAcceleratorNotify interface [DirectShow]","IAMVideoAcceleratorNotify interface [DirectShow]","described","IAMVideoAcceleratorNotifyInterface","dshow.iamvideoacceleratornotify","videoacc/IAMVideoAcceleratorNotify"]
old-location: dshow\iamvideoacceleratornotify.htm
tech.root: dshow
ms.assetid: 7fd0290c-8fd6-4af6-b510-7a87bc7937de
ms.date: 12/05/2018
ms.keywords: IAMVideoAcceleratorNotify, IAMVideoAcceleratorNotify interface [DirectShow], IAMVideoAcceleratorNotify interface [DirectShow],described, IAMVideoAcceleratorNotifyInterface, dshow.iamvideoacceleratornotify, videoacc/IAMVideoAcceleratorNotify
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
 - IAMVideoAcceleratorNotify
 - videoacc/IAMVideoAcceleratorNotify
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
 - IAMVideoAcceleratorNotify
---

# IAMVideoAcceleratorNotify interface


## -description

The <b>IAMVideoAcceleratorNotify</b> interface is a callback interface used in conjunction with the <a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator">IAMVideoAccelerator</a> interface. It enables the video renderer filter to communicate with the video decoder when configuring 
        
      DirectX Video Acceleration (DXVA) decoding.

## -inheritance

The <b>IAMVideoAcceleratorNotify</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVideoAcceleratorNotify</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/directshow-reference">DirectShow Reference</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>
