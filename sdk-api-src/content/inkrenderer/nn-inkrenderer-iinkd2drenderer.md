---
UID: NN:inkrenderer.IInkD2DRenderer
title: IInkD2DRenderer (inkrenderer.h)
author: windows-sdk-content
description: An IInkD2DRenderer object enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default InkCanvas control.
old-location: input_ink\iinkd2drenderer.htm
tech.root: input_ink
ms.assetid: d1bd910d-ce64-4424-a0e1-4f55110b0265
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInkD2DRenderer, IInkD2DRenderer interface, IInkD2DRenderer interface,described, inkrenderer/IInkD2DRenderer, input_ink.iinkd2drenderer
ms.topic: interface
f1_keywords: ["inkrenderer/IInkD2DRenderer"]
req.header: inkrenderer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
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
 - IInkD2DRenderer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkD2DRenderer interface


## -description



An <b>IInkD2DRenderer</b> object enables the rendering of ink strokes onto the designated  Direct2D device context of a Universal Windows app, instead of the default <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.controls.inkcanvas">InkCanvas</a> control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkD2DRenderer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkD2DRenderer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw">Draw</a>
</td>
<td align="left" width="63%">
Renders the ink stroke to the designated  Direct2D device context of the app.

</td>
</tr>
</table> 


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=620314">Complex ink sample</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_ink/ink-renderer-interfaces">Ink renderer interfaces</a>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620308">Ink sample</a>



<a href="https://docs.microsoft.com/windows/uwp/input-and-devices/pen-and-stylus-interactions">Pen and stylus interactions</a>



<b>Samples</b>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620312">Simple ink sample</a>
 

 

