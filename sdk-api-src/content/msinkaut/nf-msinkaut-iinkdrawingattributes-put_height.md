---
UID: NF:msinkaut.IInkDrawingAttributes.put_Height
title: IInkDrawingAttributes::put_Height
author: windows-sdk-content
description: Gets or sets the height of the pen when drawing ink with the InkDrawingAttributes object.
old-location: tablet\inkdrawingattributes_height.htm
old-project: tablet
ms.assetid: 2dc9eb94-649f-42f6-8180-abf570bdc757
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 2dc9eb94-649f-42f6-8180-abf570bdc757, Height property [Tablet PC], Height property [Tablet PC],IInkDrawingAttributes interface, IInkDrawingAttributes interface [Tablet PC],Height property, IInkDrawingAttributes.Height, IInkDrawingAttributes.put_Height, IInkDrawingAttributes::Height, IInkDrawingAttributes::get_Height, IInkDrawingAttributes::put_Height, InkDrawingAttributes.get_Height, InkDrawingAttributes.put_Height, get_Height, msinkaut/IInkDrawingAttributes::Height, msinkaut/IInkDrawingAttributes::get_Height, msinkaut/IInkDrawingAttributes::put_Height, put_Height, tablet.inkdrawingattributes_height
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkDrawingAttributes::put_Height


## -description



Gets or sets the height of the pen when drawing ink with the <a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes</a> object.



This property is read/write.


## -parameters


## -remarks



This property applies only to the <a href="https://msdn.microsoft.com/1e68f701-f012-40bb-8ee4-a47da80cb8d6">Rectangle</a> pen tip. The value represents the height of the side of the rectangle. If using the <b>Ball</b> pen tip then the height of the pen tip is equal to the <a href="https://msdn.microsoft.com/6069f9d3-061a-48ba-8161-86d6152d68f0">Width</a> property, and the <b>Height</b> property is ignored.

Precision is limited to 1/1000 (three digits to the right of the decimal point). For example, if you specify a value of 2.0006, the most precise measurement is 2.001.




## -see-also




<a href="https://msdn.microsoft.com/47106C55-FA03-4996-BCFA-D00A51AF55EE">IInkDrawingAttributes</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/1e68f701-f012-40bb-8ee4-a47da80cb8d6">InkPenTip Enumeration</a>



<a href="https://msdn.microsoft.com/13e3c2dc-99a4-4643-b8b2-48586b0eb2f0">PenTip Property</a>



<a href="https://msdn.microsoft.com/6069f9d3-061a-48ba-8161-86d6152d68f0">Width Property [InkDrawingAttributes Class]</a>
 

 

