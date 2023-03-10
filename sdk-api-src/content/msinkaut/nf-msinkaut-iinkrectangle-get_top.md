---
UID: NF:msinkaut.IInkRectangle.get_Top
title: IInkRectangle::get_Top (msinkaut.h)
description: Gets or sets the top position of the InkRectangle object. (Get)
helpviewer_keywords: ["IInkRectangle interface [Tablet PC]","Top property","IInkRectangle.Top","IInkRectangle.get_Top","IInkRectangle::Top","IInkRectangle::get_Top","IInkRectangle::put_Top","InkRectangle.get_Top","InkRectangle.put_Top","Top property [Tablet PC]","Top property [Tablet PC]","IInkRectangle interface","f97145cf-9de9-427a-9701-36c6f4286910","get_Top","msinkaut/IInkRectangle::Top","msinkaut/IInkRectangle::get_Top","msinkaut/IInkRectangle::put_Top","put_Top","tablet.inkrectangle_top"]
old-location: tablet\inkrectangle_top.htm
tech.root: tablet
ms.assetid: f97145cf-9de9-427a-9701-36c6f4286910
ms.date: 12/05/2018
ms.keywords: IInkRectangle interface [Tablet PC],Top property, IInkRectangle.Top, IInkRectangle.get_Top, IInkRectangle::Top, IInkRectangle::get_Top, IInkRectangle::put_Top, InkRectangle.get_Top, InkRectangle.put_Top, Top property [Tablet PC], Top property [Tablet PC],IInkRectangle interface, f97145cf-9de9-427a-9701-36c6f4286910, get_Top, msinkaut/IInkRectangle::Top, msinkaut/IInkRectangle::get_Top, msinkaut/IInkRectangle::put_Top, put_Top, tablet.inkrectangle_top
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
 - IInkRectangle::get_Top
 - msinkaut/IInkRectangle::get_Top
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
 - IInkRectangle.Top
 - IInkRectangle.get_Top
 - IInkRectangle.put_Top
 - InkRectangle.get_Top
 - InkRectangle.put_Top
---

# IInkRectangle::get_Top


## -description

Gets or sets the top position of the <a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object.



This property is read/write.

## -parameters

## -remarks

Note: A point is within an <a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a> if it lies on the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left">Left Property</a> or <b>Top Property</b> side or is within all four sides. A point on the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right">Right Property</a> or <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom">Bottom Property</a> side is considered outside the rectangle.

The default value of this property is 0.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom">Bottom Property</a>



<a href="../msinkaut/nn-msinkaut-iinkrectangle.md">IInkRectangle</a>



<a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left">Left Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right">Right Property</a>
