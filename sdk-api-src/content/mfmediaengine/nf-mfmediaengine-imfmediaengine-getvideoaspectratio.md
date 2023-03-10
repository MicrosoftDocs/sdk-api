---
UID: NF:mfmediaengine.IMFMediaEngine.GetVideoAspectRatio
title: IMFMediaEngine::GetVideoAspectRatio (mfmediaengine.h)
description: Gets the picture aspect ratio of the video stream.
helpviewer_keywords: ["GetVideoAspectRatio","GetVideoAspectRatio method [Media Foundation]","GetVideoAspectRatio method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetVideoAspectRatio method","IMFMediaEngine.GetVideoAspectRatio","IMFMediaEngine::GetVideoAspectRatio","mf.imfmediaengine_getvideoaspectratio","mfmediaengine/IMFMediaEngine::GetVideoAspectRatio"]
old-location: mf\imfmediaengine_getvideoaspectratio.htm
tech.root: mf
ms.assetid: 82B4AD4B-1A2E-4B03-8343-E4E5A43E62D2
ms.date: 12/05/2018
ms.keywords: GetVideoAspectRatio, GetVideoAspectRatio method [Media Foundation], GetVideoAspectRatio method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetVideoAspectRatio method, IMFMediaEngine.GetVideoAspectRatio, IMFMediaEngine::GetVideoAspectRatio, mf.imfmediaengine_getvideoaspectratio, mfmediaengine/IMFMediaEngine::GetVideoAspectRatio
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngine::GetVideoAspectRatio
 - mfmediaengine/IMFMediaEngine::GetVideoAspectRatio
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngine.GetVideoAspectRatio
---

# IMFMediaEngine::GetVideoAspectRatio


## -description

Gets the picture aspect ratio of the video stream.

## -parameters

### -param cx [out]

Receives the x component of the aspect ratio.

### -param cy [out]

Receives the y component of the aspect ratio.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The Media Engine automatically converts the pixel aspect ratio to 1:1 (square pixels).

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>



<a href="/windows/desktop/medfound/picture-aspect-ratio">Picture Aspect Ratio</a>