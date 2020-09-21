---
UID: NF:amvideo.IFullScreenVideoEx.KeepPixelAspectRatio
title: IFullScreenVideoEx::KeepPixelAspectRatio (amvideo.h)
description: The KeepPixelAspectRatio method specifies whether to maintain the pixel aspect ratio. The Full Screen Renderer filter does not support this method; it always maintains the pixel aspect ratio.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","KeepPixelAspectRatio method","IFullScreenVideoEx.KeepPixelAspectRatio","IFullScreenVideoEx::KeepPixelAspectRatio","IFullScreenVideoExKeepPixelAspectRatio","KeepPixelAspectRatio","KeepPixelAspectRatio method [DirectShow]","KeepPixelAspectRatio method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::KeepPixelAspectRatio","dshow.ifullscreenvideoex_keeppixelaspectratio"]
old-location: dshow\ifullscreenvideoex_keeppixelaspectratio.htm
tech.root: dshow
ms.assetid: f2c57560-7ffa-4bd4-8d0c-a048dafa35bc
ms.date: 12/05/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],KeepPixelAspectRatio method, IFullScreenVideoEx.KeepPixelAspectRatio, IFullScreenVideoEx::KeepPixelAspectRatio, IFullScreenVideoExKeepPixelAspectRatio, KeepPixelAspectRatio, KeepPixelAspectRatio method [DirectShow], KeepPixelAspectRatio method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::KeepPixelAspectRatio, dshow.ifullscreenvideoex_keeppixelaspectratio
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
 - IFullScreenVideoEx::KeepPixelAspectRatio
 - amvideo/IFullScreenVideoEx::KeepPixelAspectRatio
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
 - IFullScreenVideoEx.KeepPixelAspectRatio
---

# IFullScreenVideoEx::KeepPixelAspectRatio


## -description

The <code>KeepPixelAspectRatio</code> method specifies whether to maintain the pixel aspect ratio. The Full Screen Renderer filter does not support this method; it always maintains the pixel aspect ratio.

## -parameters

### -param KeepAspect [in]

Specifies whether to maintain the aspect ratio. The value must be OATRUE or OAFALSE.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>