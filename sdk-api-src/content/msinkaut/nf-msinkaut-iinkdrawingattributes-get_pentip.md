---
UID: NF:msinkaut.IInkDrawingAttributes.get_PenTip
title: IInkDrawingAttributes::get_PenTip (msinkaut.h)
description: Gets or sets a value that indicates which pen tip to use when drawing ink that is associated with this InkDrawingAttributes object.helpviewer_keywords: ["13e3c2dc-99a4-4643-b8b2-48586b0eb2f0","IInkDrawingAttributes interface [Tablet PC]","PenTip property","IInkDrawingAttributes.PenTip","IInkDrawingAttributes.get_PenTip","IInkDrawingAttributes::PenTip","IInkDrawingAttributes::get_PenTip","IInkDrawingAttributes::put_PenTip","InkDrawingAttributes.get_PenTip","InkDrawingAttributes.put_PenTip","PenTip property [Tablet PC]","PenTip property [Tablet PC]","IInkDrawingAttributes interface","get_PenTip","msinkaut/IInkDrawingAttributes::PenTip","msinkaut/IInkDrawingAttributes::get_PenTip","msinkaut/IInkDrawingAttributes::put_PenTip","put_PenTip","tablet.inkdrawingattributes_pentip"]
old-location: tablet\inkdrawingattributes_pentip.htm
tech.root: tablet
ms.assetid: 13e3c2dc-99a4-4643-b8b2-48586b0eb2f0
ms.date: 12/05/2018
ms.keywords: 13e3c2dc-99a4-4643-b8b2-48586b0eb2f0, IInkDrawingAttributes interface [Tablet PC],PenTip property, IInkDrawingAttributes.PenTip, IInkDrawingAttributes.get_PenTip, IInkDrawingAttributes::PenTip, IInkDrawingAttributes::get_PenTip, IInkDrawingAttributes::put_PenTip, InkDrawingAttributes.get_PenTip, InkDrawingAttributes.put_PenTip, PenTip property [Tablet PC], PenTip property [Tablet PC],IInkDrawingAttributes interface, get_PenTip, msinkaut/IInkDrawingAttributes::PenTip, msinkaut/IInkDrawingAttributes::get_PenTip, msinkaut/IInkDrawingAttributes::put_PenTip, put_PenTip, tablet.inkdrawingattributes_pentip
f1_keywords:
- msinkaut/IInkDrawingAttributes.PenTip
dev_langs:
- c++
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
- IInkDrawingAttributes.PenTip
- IInkDrawingAttributes.get_PenTip
- IInkDrawingAttributes.put_PenTip
- InkDrawingAttributes.get_PenTip
- InkDrawingAttributes.put_PenTip
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDrawingAttributes::get_PenTip


## -description



Gets or sets a value that indicates which pen tip to use when drawing ink that is associated with this <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> object.



This property is read/write.


## -parameters


## -remarks



For a complete list of pen tips available to use, see the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkpentip">InkPenTip</a> enumeration.

When this property is set to <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkpentip">InkPenTip.IPT_Ball</a>, the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height">Height</a> property is ignored.

To create a square pen tip, set the <b>PenTip</b> property to <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkpentip">InkPenTip.IPT_Rectangle</a>. Then set the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height">Height</a> property equal to the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width">Width</a> property.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height">Height Property [InkDrawingAttributes Class]</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846798(v=VS.85).aspx">IInkDrawingAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkpentip">InkPenTip Enumeration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width">Width Property [InkDrawingAttributes Class]</a>
 

 

