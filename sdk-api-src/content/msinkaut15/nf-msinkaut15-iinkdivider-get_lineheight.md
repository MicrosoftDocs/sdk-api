---
UID: NF:msinkaut15.IInkDivider.get_LineHeight
title: IInkDivider::get_LineHeight (msinkaut15.h)
author: windows-sdk-content
description: Gets or sets the expected handwriting height, in HIMETRIC units.
old-location: tablet\inkdivider_lineheight.htm
tech.root: tablet
ms.assetid: 69e65ad6-bcee-46a7-a139-80b4324b9c72
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 69e65ad6-bcee-46a7-a139-80b4324b9c72, IInkDivider interface [Tablet PC],LineHeight property, IInkDivider.LineHeight, IInkDivider.get_LineHeight, IInkDivider::LineHeight, IInkDivider::get_LineHeight, IInkDivider::put_LineHeight, InkDivider.get_LineHeight, InkDivider.put_LineHeight, LineHeight property [Tablet PC], LineHeight property [Tablet PC],IInkDivider interface, get_LineHeight, msinkaut15/IInkDivider::LineHeight, msinkaut15/IInkDivider::get_LineHeight, msinkaut15/IInkDivider::put_LineHeight, put_LineHeight, tablet.inkdivider_lineheight
ms.topic: method
f1_keywords: 
 - "msinkaut15/IInkDivider.LineHeight"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDivider::get_LineHeight


## -description



Gets or sets the expected handwriting height, in HIMETRIC units.



This property is read/write.


## -parameters


## -remarks



The <b>LineHeight</b> property must be in the range of 100 to 50,000 HIMETRIC units.

The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider</a> object uses the <b>LineHeight</b> property to help distinguish between drawing and handwriting.

Setting the <b>LineHeight</b> property after strokes have been assigned to the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider</a> object generates an error.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt847144(v=VS.85).aspx">IInkDivider</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdivider-class">InkDivider Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes">Strokes Property [InkDivider Class]</a>
 

 

