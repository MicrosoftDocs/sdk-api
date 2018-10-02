---
UID: NF:msinkaut15.IInkDivider.put_LineHeight
title: IInkDivider::put_LineHeight
author: windows-sdk-content
description: Gets or sets the expected handwriting height, in HIMETRIC units.
old-location: tablet\inkdivider_lineheight.htm
tech.root: tablet
ms.assetid: 69e65ad6-bcee-46a7-a139-80b4324b9c72
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 69e65ad6-bcee-46a7-a139-80b4324b9c72, IInkDivider interface [Tablet PC],LineHeight property, IInkDivider.LineHeight, IInkDivider.put_LineHeight, IInkDivider::LineHeight, IInkDivider::get_LineHeight, IInkDivider::put_LineHeight, InkDivider.get_LineHeight, InkDivider.put_LineHeight, LineHeight property [Tablet PC], LineHeight property [Tablet PC],IInkDivider interface, get_LineHeight, msinkaut15/IInkDivider::LineHeight, msinkaut15/IInkDivider::get_LineHeight, msinkaut15/IInkDivider::put_LineHeight, put_LineHeight, tablet.inkdivider_lineheight
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut15.h
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
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inkdiv.dll
 - Inkdiv.dll.dll
api_name:
 - IInkDivider.LineHeight
 - IInkDivider.get_LineHeight
 - IInkDivider.put_LineHeight
 - InkDivider.get_LineHeight
 - InkDivider.put_LineHeight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDivider::put_LineHeight


## -description



Gets or sets the expected handwriting height, in HIMETRIC units.



This property is read/write.


## -parameters


## -remarks



The <b>LineHeight</b> property must be in the range of 100 to 50,000 HIMETRIC units.

The <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object uses the <b>LineHeight</b> property to help distinguish between drawing and handwriting.

Setting the <b>LineHeight</b> property after strokes have been assigned to the <a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider</a> object generates an error.




## -see-also




<a href="https://msdn.microsoft.com/6DF54C8E-1E0D-4F9D-A6E4-AFE0E8894BE9">IInkDivider</a>



<a href="https://msdn.microsoft.com/2c8e67fb-1032-4fcc-b419-82bae978daf8">InkDivider Class</a>



<a href="https://msdn.microsoft.com/611ccce9-7acb-4138-9655-938efcaa4c75">Strokes Property [InkDivider Class]</a>
 

 

