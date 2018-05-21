---
UID: NF:amvideo.IFullScreenVideoEx.KeepPixelAspectRatio
title: IFullScreenVideoEx::KeepPixelAspectRatio
author: windows-driver-content
description: The KeepPixelAspectRatio method specifies whether to maintain the pixel aspect ratio. The Full Screen Renderer filter does not support this method; it always maintains the pixel aspect ratio.
old-location: dshow\ifullscreenvideoex_keeppixelaspectratio.htm
old-project: DirectShow
ms.assetid: f2c57560-7ffa-4bd4-8d0c-a048dafa35bc
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],KeepPixelAspectRatio method, IFullScreenVideoEx.KeepPixelAspectRatio, IFullScreenVideoEx::KeepPixelAspectRatio, IFullScreenVideoExKeepPixelAspectRatio, KeepPixelAspectRatio, KeepPixelAspectRatio method [DirectShow], KeepPixelAspectRatio method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::KeepPixelAspectRatio, dshow.ifullscreenvideoex_keeppixelaspectratio
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IFullScreenVideoEx.KeepPixelAspectRatio
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

