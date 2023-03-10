---
UID: NF:msinkaut.IInkDrawingAttributes.get_Transparency
title: IInkDrawingAttributes::get_Transparency (msinkaut.h)
description: Gets or sets a value that indicates the transparency value of ink. (Get)
helpviewer_keywords: ["IInkDrawingAttributes interface [Tablet PC]","Transparency property","IInkDrawingAttributes.Transparency","IInkDrawingAttributes.get_Transparency","IInkDrawingAttributes::Transparency","IInkDrawingAttributes::get_Transparency","IInkDrawingAttributes::put_Transparency","InkDrawingAttributes.get_Transparency","InkDrawingAttributes.put_Transparency","Transparency property [Tablet PC]","Transparency property [Tablet PC]","IInkDrawingAttributes interface","e1537635-3457-429e-bb72-33eb4a2ea3da","get_Transparency","msinkaut/IInkDrawingAttributes::Transparency","msinkaut/IInkDrawingAttributes::get_Transparency","msinkaut/IInkDrawingAttributes::put_Transparency","put_Transparency","tablet.inkdrawingattributes_transparency"]
old-location: tablet\inkdrawingattributes_transparency.htm
tech.root: tablet
ms.assetid: e1537635-3457-429e-bb72-33eb4a2ea3da
ms.date: 12/05/2018
ms.keywords: IInkDrawingAttributes interface [Tablet PC],Transparency property, IInkDrawingAttributes.Transparency, IInkDrawingAttributes.get_Transparency, IInkDrawingAttributes::Transparency, IInkDrawingAttributes::get_Transparency, IInkDrawingAttributes::put_Transparency, InkDrawingAttributes.get_Transparency, InkDrawingAttributes.put_Transparency, Transparency property [Tablet PC], Transparency property [Tablet PC],IInkDrawingAttributes interface, e1537635-3457-429e-bb72-33eb4a2ea3da, get_Transparency, msinkaut/IInkDrawingAttributes::Transparency, msinkaut/IInkDrawingAttributes::get_Transparency, msinkaut/IInkDrawingAttributes::put_Transparency, put_Transparency, tablet.inkdrawingattributes_transparency
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDrawingAttributes::get_Transparency
 - msinkaut/IInkDrawingAttributes::get_Transparency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkDrawingAttributes.Transparency
 - IInkDrawingAttributes.get_Transparency
 - IInkDrawingAttributes.put_Transparency
 - InkDrawingAttributes.get_Transparency
 - InkDrawingAttributes.put_Transparency
---

# IInkDrawingAttributes::get_Transparency


## -description

Gets or sets a value that indicates the transparency value of ink.



This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  The transparent rendering effect may be different between dynamic and static rendering. In dynamic rendering the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object is rendered as it is drawn, as it is in the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering">DynamicRendering</a> property, for example. In static rendering, you use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw">Draw</a> method of the <a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer</a> object to render the <b>IInkStrokeDisp</b> object.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw">Draw Method [InkRenderer Class]</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke">DrawStroke Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering">DynamicRendering Property</a>



<a href="../msinkaut/nn-msinkaut-iinkdrawingattributes.md">IInkDrawingAttributes</a>



<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>



<a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer Class</a>
