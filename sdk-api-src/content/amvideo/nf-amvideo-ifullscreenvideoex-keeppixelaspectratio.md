---
UID: NF:amvideo.IFullScreenVideoEx.KeepPixelAspectRatio
title: IFullScreenVideoEx::KeepPixelAspectRatio (amvideo.h)
author: windows-sdk-content
description: The KeepPixelAspectRatio method specifies whether to maintain the pixel aspect ratio. The Full Screen Renderer filter does not support this method; it always maintains the pixel aspect ratio.
old-location: dshow\ifullscreenvideoex_keeppixelaspectratio.htm
tech.root: DirectShow
ms.assetid: f2c57560-7ffa-4bd4-8d0c-a048dafa35bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],KeepPixelAspectRatio method, IFullScreenVideoEx.KeepPixelAspectRatio, IFullScreenVideoEx::KeepPixelAspectRatio, IFullScreenVideoExKeepPixelAspectRatio, KeepPixelAspectRatio, KeepPixelAspectRatio method [DirectShow], KeepPixelAspectRatio method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::KeepPixelAspectRatio, dshow.ifullscreenvideoex_keeppixelaspectratio
ms.topic: method
f1_keywords: ["amvideo/IFullScreenVideoEx.KeepPixelAspectRatio"]
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
 - IFullScreenVideoEx.KeepPixelAspectRatio
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>
 

 

