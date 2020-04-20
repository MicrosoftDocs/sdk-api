---
UID: NF:msinkaut.IInkRectangle.put_Right
title: IInkRectangle::put_Right (msinkaut.h)
description: Gets or sets the right position of the InkRectangle object.helpviewer_keywords: ["IInkRectangle interface [Tablet PC]","Right property","IInkRectangle.Right","IInkRectangle.put_Right","IInkRectangle::Right","IInkRectangle::get_Right","IInkRectangle::put_Right","InkRectangle.get_Right","InkRectangle.put_Right","Right property [Tablet PC]","Right property [Tablet PC]","IInkRectangle interface","c31fd527-a6aa-4017-bc51-cedca42817f9","get_Right","msinkaut/IInkRectangle::Right","msinkaut/IInkRectangle::get_Right","msinkaut/IInkRectangle::put_Right","put_Right","tablet.inkrectangle_right"]
old-location: tablet\inkrectangle_right.htm
tech.root: tablet
ms.assetid: c31fd527-a6aa-4017-bc51-cedca42817f9
ms.date: 12/05/2018
ms.keywords: IInkRectangle interface [Tablet PC],Right property, IInkRectangle.Right, IInkRectangle.put_Right, IInkRectangle::Right, IInkRectangle::get_Right, IInkRectangle::put_Right, InkRectangle.get_Right, InkRectangle.put_Right, Right property [Tablet PC], Right property [Tablet PC],IInkRectangle interface, c31fd527-a6aa-4017-bc51-cedca42817f9, get_Right, msinkaut/IInkRectangle::Right, msinkaut/IInkRectangle::get_Right, msinkaut/IInkRectangle::put_Right, put_Right, tablet.inkrectangle_right
f1_keywords:
- msinkaut/IInkRectangle.Right
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
- IInkRectangle.Right
- IInkRectangle.get_Right
- IInkRectangle.put_Right
- InkRectangle.get_Right
- InkRectangle.put_Right
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRectangle::put_Right


## -description



Gets or sets the right position of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object.



This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  A point is within an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> if it lies on the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left">Left</a> or <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top">Top</a> side or is within all four sides. A point on the <b>Right</b> or <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom">Bottom</a> side is considered outside the rectangle.</div>
<div> </div>
The default value of this property is 0.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom">Bottom Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846804(v=VS.85).aspx">IInkRectangle</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left">Left Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top">Top Property</a>
 

 

