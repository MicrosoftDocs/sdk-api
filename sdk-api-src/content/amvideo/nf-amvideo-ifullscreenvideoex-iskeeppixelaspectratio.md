---
UID: NF:amvideo.IFullScreenVideoEx.IsKeepPixelAspectRatio
title: IFullScreenVideoEx::IsKeepPixelAspectRatio
author: windows-sdk-content
description: The IsKeepPixelAspectRatio method queries whether the pixel aspect ratio is maintained. The Full Screen Renderer filter does not support this method; it always maintains the pixel aspect ratio.
old-location: dshow\ifullscreenvideoex_iskeeppixelaspectratio.htm
tech.root: DirectShow
ms.assetid: 3f3b55d9-b504-42a3-b60a-65073d1e1447
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],IsKeepPixelAspectRatio method, IFullScreenVideoEx.IsKeepPixelAspectRatio, IFullScreenVideoEx::IsKeepPixelAspectRatio, IFullScreenVideoExIsKeepPixelAspectRatio, IsKeepPixelAspectRatio, IsKeepPixelAspectRatio method [DirectShow], IsKeepPixelAspectRatio method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::IsKeepPixelAspectRatio, dshow.ifullscreenvideoex_iskeeppixelaspectratio
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4c9de58f-6ceb-4cf5-b1a5-d3e345e08190">IFullScreenVideoEx Interface</a>
 

 

