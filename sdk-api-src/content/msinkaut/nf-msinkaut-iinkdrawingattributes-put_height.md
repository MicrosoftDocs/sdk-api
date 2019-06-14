---
UID: NF:msinkaut.IInkDrawingAttributes.put_Height
title: IInkDrawingAttributes::put_Height (msinkaut.h)
author: windows-sdk-content
description: Gets or sets the height of the pen when drawing ink with the InkDrawingAttributes object.
old-location: tablet\inkdrawingattributes_height.htm
tech.root: tablet
ms.assetid: 2dc9eb94-649f-42f6-8180-abf570bdc757
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 2dc9eb94-649f-42f6-8180-abf570bdc757, Height property [Tablet PC], Height property [Tablet PC],IInkDrawingAttributes interface, IInkDrawingAttributes interface [Tablet PC],Height property, IInkDrawingAttributes.Height, IInkDrawingAttributes.put_Height, IInkDrawingAttributes::Height, IInkDrawingAttributes::get_Height, IInkDrawingAttributes::put_Height, InkDrawingAttributes.get_Height, InkDrawingAttributes.put_Height, get_Height, msinkaut/IInkDrawingAttributes::Height, msinkaut/IInkDrawingAttributes::get_Height, msinkaut/IInkDrawingAttributes::put_Height, put_Height, tablet.inkdrawingattributes_height
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
 - IInkDrawingAttributes.Height
 - IInkDrawingAttributes.get_Height
 - IInkDrawingAttributes.put_Height
 - InkDrawingAttributes.get_Height
 - InkDrawingAttributes.put_Height
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDrawingAttributes::put_Height


## -description



Gets or sets the height of the pen when drawing ink with the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> object.



This property is read/write.


## -parameters


## -remarks



This property applies only to the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkpentip">Rectangle</a> pen tip. The value represents the height of the side of the rectangle. If using the <b>Ball</b> pen tip then the height of the pen tip is equal to the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width">Width</a> property, and the <b>Height</b> property is ignored.

Precision is limited to 1/1000 (three digits to the right of the decimal point). For example, if you specify a value of 2.0006, the most precise measurement is 2.001.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846798(v=VS.85).aspx">IInkDrawingAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkpentip">InkPenTip Enumeration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip">PenTip Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width">Width Property [InkDrawingAttributes Class]</a>
 

 

