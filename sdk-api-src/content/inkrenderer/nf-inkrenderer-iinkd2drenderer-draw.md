---
UID: NF:inkrenderer.IInkD2DRenderer.Draw
title: IInkD2DRenderer::Draw (inkrenderer.h)
author: windows-sdk-content
description: Renders the ink stroke to the designated Direct2D device context of the app.
old-location: input_ink\iinkd2drenderer_draw.htm
tech.root: input_ink
ms.assetid: 013f3b95-d5da-44e3-b2da-64a49cc8908e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Draw, Draw method, Draw method,IInkD2DRenderer interface, IInkD2DRenderer interface,Draw method, IInkD2DRenderer.Draw, IInkD2DRenderer::Draw, inkrenderer/IInkD2DRenderer::Draw, input_ink.iinkd2drenderer_draw
ms.topic: method
f1_keywords: ["inkrenderer/IInkD2DRenderer.Draw"]
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Listen for the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.viewmanagement.accessibilitysettings.highcontrastchanged">HighContrastChanged</a> event to set this value appropriately.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=620314">Complex ink sample</a>



<a href="https://docs.microsoft.com/windows/desktop/api/inkrenderer/nn-inkrenderer-iinkd2drenderer">IInkD2DRenderer</a>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620308">Ink sample</a>



<a href="https://docs.microsoft.com/windows/uwp/input-and-devices/pen-and-stylus-interactions">Pen and stylus interactions</a>



<b>Samples</b>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620312">Simple ink sample</a>
 

 

