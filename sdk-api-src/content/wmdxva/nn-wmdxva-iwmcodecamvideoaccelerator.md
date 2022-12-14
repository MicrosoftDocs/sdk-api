---
UID: NN:wmdxva.IWMCodecAMVideoAccelerator
title: IWMCodecAMVideoAccelerator (wmdxva.h)
description: This interface is exposed by the Windows Media Decoder DMO and is called by a media player source filter to set up the various connections required to enable DirectX&#174; video acceleration (VA) for decoding of Windows Media-based video content.
helpviewer_keywords: ["IWMCodecAMVideoAccelerator","IWMCodecAMVideoAccelerator interface [windows Media Format]","IWMCodecAMVideoAccelerator interface [windows Media Format]","described","IWMCodecAMVideoAcceleratorInterface","wmdxva/IWMCodecAMVideoAccelerator","wmformat.iwmcodecamvideoaccelerator"]
old-location: wmformat\iwmcodecamvideoaccelerator.htm
tech.root: wmformat
ms.assetid: 48cfc4d1-4b79-47a5-9cc9-a1f19d2c0123
ms.date: 12/05/2018
ms.keywords: IWMCodecAMVideoAccelerator, IWMCodecAMVideoAccelerator interface [windows Media Format], IWMCodecAMVideoAccelerator interface [windows Media Format],described, IWMCodecAMVideoAcceleratorInterface, wmdxva/IWMCodecAMVideoAccelerator, wmformat.iwmcodecamvideoaccelerator
req.header: wmdxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IWMCodecAMVideoAccelerator
 - wmdxva/IWMCodecAMVideoAccelerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmdxva.h
api_name:
 - IWMCodecAMVideoAccelerator
---

# IWMCodecAMVideoAccelerator interface


## -description

This interface is exposed by the Windows Media Decoder <a href="/windows/desktop/wmformat/wmformat-glossary">DMO</a> and is called by a media player source filter to set up the various connections required to enable DirectX® video acceleration (VA) for decoding of Windows Media-based video content. A player obtains this interface by calling the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderaccelerator-getcodecinterface">IWMReaderAccelerator::GetCodecInterface</a> method, which is exposed on the reader object.

## -inheritance

The <b>IWMCodecAMVideoAccelerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMCodecAMVideoAccelerator</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>
