---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

