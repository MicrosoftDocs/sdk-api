---
UID: NF:msinkaut.IInkDrawingAttributes.put_PenTip
title: IInkDrawingAttributes::put_PenTip
author: windows-sdk-content
description: Gets or sets a value that indicates which pen tip to use when drawing ink that is associated with this InkDrawingAttributes object.
old-location: tablet\inkdrawingattributes_pentip.htm
tech.root: tablet
ms.assetid: 13e3c2dc-99a4-4643-b8b2-48586b0eb2f0
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: 13e3c2dc-99a4-4643-b8b2-48586b0eb2f0, IInkDrawingAttributes interface [Tablet PC],PenTip property, IInkDrawingAttributes.PenTip, IInkDrawingAttributes.put_PenTip, IInkDrawingAttributes::PenTip, IInkDrawingAttributes::get_PenTip, IInkDrawingAttributes::put_PenTip, InkDrawingAttributes.get_PenTip, InkDrawingAttributes.put_PenTip, PenTip property [Tablet PC], PenTip property [Tablet PC],IInkDrawingAttributes interface, get_PenTip, msinkaut/IInkDrawingAttributes::PenTip, msinkaut/IInkDrawingAttributes::get_PenTip, msinkaut/IInkDrawingAttributes::put_PenTip, put_PenTip, tablet.inkdrawingattributes_pentip
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
 - IInkDrawingAttributes.PenTip
 - IInkDrawingAttributes.get_PenTip
 - IInkDrawingAttributes.put_PenTip
 - InkDrawingAttributes.get_PenTip
 - InkDrawingAttributes.put_PenTip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDrawingAttributes::put_PenTip


## -description



Gets or sets a value that indicates which pen tip to use when drawing ink that is associated with this <a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes</a> object.



This property is read/write.


## -parameters


## -remarks



For a complete list of pen tips available to use, see the <a href="https://msdn.microsoft.com/1e68f701-f012-40bb-8ee4-a47da80cb8d6">InkPenTip</a> enumeration.

When this property is set to <a href="https://msdn.microsoft.com/1e68f701-f012-40bb-8ee4-a47da80cb8d6">InkPenTip.IPT_Ball</a>, the <a href="https://msdn.microsoft.com/2dc9eb94-649f-42f6-8180-abf570bdc757">Height</a> property is ignored.

To create a square pen tip, set the <b>PenTip</b> property to <a href="https://msdn.microsoft.com/1e68f701-f012-40bb-8ee4-a47da80cb8d6">InkPenTip.IPT_Rectangle</a>. Then set the <a href="https://msdn.microsoft.com/2dc9eb94-649f-42f6-8180-abf570bdc757">Height</a> property equal to the <a href="https://msdn.microsoft.com/6069f9d3-061a-48ba-8161-86d6152d68f0">Width</a> property.




## -see-also




<a href="https://msdn.microsoft.com/2dc9eb94-649f-42f6-8180-abf570bdc757">Height Property [InkDrawingAttributes Class]</a>



<a href="https://msdn.microsoft.com/47106C55-FA03-4996-BCFA-D00A51AF55EE">IInkDrawingAttributes</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/1e68f701-f012-40bb-8ee4-a47da80cb8d6">InkPenTip Enumeration</a>



<a href="https://msdn.microsoft.com/6069f9d3-061a-48ba-8161-86d6152d68f0">Width Property [InkDrawingAttributes Class]</a>
 

 

