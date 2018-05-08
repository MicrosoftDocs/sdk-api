---
UID: NN:inkrenderer.IInkD2DRenderer
title: IInkD2DRenderer
author: windows-driver-content
description: An IInkD2DRenderer object enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default InkCanvas control.
old-location: input_ink\iinkd2drenderer.htm
old-project: input_ink
ms.assetid: d1bd910d-ce64-4424-a0e1-4f55110b0265
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IInkD2DRenderer, IInkD2DRenderer interface, IInkD2DRenderer interface,described, inkrenderer/IInkD2DRenderer, input_ink.iinkd2drenderer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: inkrenderer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps | UWP apps]
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	inkrenderer.h
api_name:
-	IInkD2DRenderer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkD2DRenderer interface


## -description



An <b>IInkD2DRenderer</b> object enables the rendering of ink strokes onto the designated  Direct2D device context of a Universal Windows app, instead of the default <a href="https://msdn.microsoft.com/28087708-d2f8-4684-a61a-abfba05b0592">InkCanvas</a> control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkD2DRenderer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkD2DRenderer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInkD2DRenderer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/013f3b95-d5da-44e3-b2da-64a49cc8908e">Draw</a>
</td>
<td align="left" width="63%">
Renders the ink stroke to the designated  Direct2D device context of the app.

</td>
</tr>
</table> 


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=620314">Complex ink sample</a>



<a href="https://msdn.microsoft.com/8589130C-AC31-42A1-B248-11AA26EC34D4">Ink renderer interfaces</a>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620308">Ink sample</a>



<a href="https://msdn.microsoft.com/3DA4F2D2-5405-42A1-9ED9-3A87BCD84C43">Pen and stylus interactions</a>



<b>Samples</b>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620312">Simple ink sample</a>
 

 

