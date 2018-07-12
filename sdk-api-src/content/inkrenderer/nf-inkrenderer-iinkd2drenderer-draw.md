---
UID: NF:inkrenderer.IInkD2DRenderer.Draw
title: IInkD2DRenderer::Draw
author: windows-sdk-content
description: Renders the ink stroke to the designated Direct2D device context of the app.
old-location: input_ink\iinkd2drenderer_draw.htm
old-project: input_ink
ms.assetid: 013f3b95-d5da-44e3-b2da-64a49cc8908e
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: Draw, Draw method, Draw method,IInkD2DRenderer interface, IInkD2DRenderer interface,Draw method, IInkD2DRenderer.Draw, IInkD2DRenderer::Draw, inkrenderer/IInkD2DRenderer::Draw, input_ink.iinkd2drenderer_draw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: inkrenderer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Inkrenderer.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - inkrenderer.h
api_name:
 - IInkD2DRenderer.Draw
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkD2DRenderer::Draw


## -description



Renders the ink stroke to the designated  Direct2D device context of the app.




## -parameters




### -param pD2D1DeviceContext [in]

Pointer to the designated Direct2D device context of the app.


### -param pInkStrokeIterable [in]

Pointer to the collection of ink strokes to render.


### -param fHighContrast [in]

True, if the Windows high-contrast accessibility option is currently selected. Otherwise, false.

Listen for the <a href="https://msdn.microsoft.com/a0ca0b9b-4291-40a9-b5dd-de26d0e35bd1">HighContrastChanged</a> event to set this value appropriately.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=620314">Complex ink sample</a>



<a href="https://msdn.microsoft.com/d1bd910d-ce64-4424-a0e1-4f55110b0265">IInkD2DRenderer</a>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620308">Ink sample</a>



<a href="https://msdn.microsoft.com/3DA4F2D2-5405-42A1-9ED9-3A87BCD84C43">Pen and stylus interactions</a>



<b>Samples</b>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620312">Simple ink sample</a>
 

 

