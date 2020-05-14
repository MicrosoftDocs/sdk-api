---
UID: NF:amvideo.IFullScreenVideoEx.IsKeepPixelAspectRatio
title: IFullScreenVideoEx::IsKeepPixelAspectRatio (amvideo.h)
description: The IsKeepPixelAspectRatio method queries whether the pixel aspect ratio is maintained. The Full Screen Renderer filter does not support this method; it always maintains the pixel aspect ratio.helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","IsKeepPixelAspectRatio method","IFullScreenVideoEx.IsKeepPixelAspectRatio","IFullScreenVideoEx::IsKeepPixelAspectRatio","IFullScreenVideoExIsKeepPixelAspectRatio","IsKeepPixelAspectRatio","IsKeepPixelAspectRatio method [DirectShow]","IsKeepPixelAspectRatio method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::IsKeepPixelAspectRatio","dshow.ifullscreenvideoex_iskeeppixelaspectratio"]
old-location: dshow\ifullscreenvideoex_iskeeppixelaspectratio.htm
tech.root: DirectShow
ms.assetid: 3f3b55d9-b504-42a3-b60a-65073d1e1447
ms.date: 12/05/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],IsKeepPixelAspectRatio method, IFullScreenVideoEx.IsKeepPixelAspectRatio, IFullScreenVideoEx::IsKeepPixelAspectRatio, IFullScreenVideoExIsKeepPixelAspectRatio, IsKeepPixelAspectRatio, IsKeepPixelAspectRatio method [DirectShow], IsKeepPixelAspectRatio method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::IsKeepPixelAspectRatio, dshow.ifullscreenvideoex_iskeeppixelaspectratio
f1_keywords:
- amvideo/IFullScreenVideoEx.IsKeepPixelAspectRatio
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IFullScreenVideoEx.IsKeepPixelAspectRatio
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFullScreenVideoEx::IsKeepPixelAspectRatio


## -description



The <code>IsKeepPixelAspectRatio</code> method queries whether the pixel aspect ratio is maintained. The Full Screen Renderer filter does not support this method; it always maintains the pixel aspect ratio.




## -parameters




### -param pKeepAspect [in]

Pointer to a variable that receives the value OATRUE or OAFALSE.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>
 

 

