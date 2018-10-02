---
UID: NF:gdipluspen.Pen.SetLineJoin
title: Pen::SetLineJoin
author: windows-sdk-content
description: The Pen::SetLineJoin method sets the line join for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetLineJoin_lineJoin_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setlinejoin.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Pen class [GDI+],SetLineJoin method, Pen.SetLineJoin, Pen::SetLineJoin, SetLineJoin, SetLineJoin method [GDI+], SetLineJoin method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetLineJoin_lineJoin_, gdiplus._gdiplus_CLASS_Pen_SetLineJoin_lineJoin_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspen.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Pen.SetLineJoin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::SetLineJoin


## -description


The <b>Pen::SetLineJoin</b> method sets the line join for this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters




### -param lineJoin [in]

Type: <b><a href="https://msdn.microsoft.com/7fd13263-10c9-45b1-99b4-a8da574a26f3">LineJoin</a></b>

Element of the 
					<a href="https://msdn.microsoft.com/7fd13263-10c9-45b1-99b4-a8da574a26f3">LineJoin</a> enumeration that specifies the join style used at the end of a line segment that meets another line segment. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/4ec3e76a-2531-4869-a5b0-c595198e8345">Joining Lines</a>



<a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/ba247773-7e9f-4130-a14c-42c3153e4da5">Pen::GetEndCap</a>



<a href="https://msdn.microsoft.com/4024524a-f139-4ec5-8788-b071658b8374">Pen::GetStartCap</a>



<a href="https://msdn.microsoft.com/ea29dcf3-7c3e-44bd-957b-0e7c46592de3">Pen::SetEndCap</a>



<a href="https://msdn.microsoft.com/2e52ce66-a567-42b9-ae47-2957ac3e0723">Pen::SetLineCap</a>



<a href="https://msdn.microsoft.com/e8289147-5154-4780-ae8f-65427093aaa3">Pen::SetStartCap</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>
 

 

