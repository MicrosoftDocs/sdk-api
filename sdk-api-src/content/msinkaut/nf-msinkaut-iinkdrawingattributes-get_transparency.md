---
UID: NF:msinkaut.IInkDrawingAttributes.get_Transparency
title: IInkDrawingAttributes::get_Transparency
author: windows-sdk-content
description: Gets or sets a value that indicates the transparency value of ink.
old-location: tablet\inkdrawingattributes_transparency.htm
tech.root: tablet
ms.assetid: e1537635-3457-429e-bb72-33eb4a2ea3da
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IInkDrawingAttributes interface [Tablet PC],Transparency property, IInkDrawingAttributes.Transparency, IInkDrawingAttributes.get_Transparency, IInkDrawingAttributes::Transparency, IInkDrawingAttributes::get_Transparency, IInkDrawingAttributes::put_Transparency, InkDrawingAttributes.get_Transparency, InkDrawingAttributes.put_Transparency, Transparency property [Tablet PC], Transparency property [Tablet PC],IInkDrawingAttributes interface, e1537635-3457-429e-bb72-33eb4a2ea3da, get_Transparency, msinkaut/IInkDrawingAttributes::Transparency, msinkaut/IInkDrawingAttributes::get_Transparency, msinkaut/IInkDrawingAttributes::put_Transparency, put_Transparency, tablet.inkdrawingattributes_transparency
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDrawingAttributes::get_Transparency


## -description



Gets or sets a value that indicates the transparency value of ink.



This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  The transparent rendering effect may be different between dynamic and static rendering. In dynamic rendering the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object is rendered as it is drawn, as it is in the <a href="https://msdn.microsoft.com/1e0e231a-82bc-4d22-9467-4c7b29f4b405">DynamicRendering</a> property, for example. In static rendering, you use the <a href="https://msdn.microsoft.com/18f67080-ed56-43af-b0d6-8af35c2e871b">Draw</a> method of the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> object to render the <b>IInkStrokeDisp</b> object.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/18f67080-ed56-43af-b0d6-8af35c2e871b">Draw Method [InkRenderer Class]</a>



<a href="https://msdn.microsoft.com/3d8b7892-a120-452a-b83c-474df9be5f52">DrawStroke Method</a>



<a href="https://msdn.microsoft.com/1e0e231a-82bc-4d22-9467-4c7b29f4b405">DynamicRendering Property</a>



<a href="https://msdn.microsoft.com/47106C55-FA03-4996-BCFA-D00A51AF55EE">IInkDrawingAttributes</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>
 

 

