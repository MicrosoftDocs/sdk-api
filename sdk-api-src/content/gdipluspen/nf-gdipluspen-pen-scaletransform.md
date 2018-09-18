---
UID: NF:gdipluspen.Pen.ScaleTransform
title: Pen::ScaleTransform
author: windows-sdk-content
description: The Pen::ScaleTransform method sets the Pen object's world transformation matrix equal to the product of itself and a scaling matrix.
old-location: gdiplus\_gdiplus_CLASS_Pen_ScaleTransform_sx_sy_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\scaletransform_26sx_sy_order.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: Pen class [GDI+],ScaleTransform method, Pen.ScaleTransform, Pen::ScaleTransform, ScaleTransform, ScaleTransform method [GDI+], ScaleTransform method [GDI+],Pen class, _gdiplus_CLASS_Pen_ScaleTransform_sx_sy_order_, gdiplus._gdiplus_CLASS_Pen_ScaleTransform_sx_sy_order_
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
 - Pen.ScaleTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::ScaleTransform


## -description


The <b>Pen::ScaleTransform</b> method sets the 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object's world transformation matrix equal to the product of itself and a scaling matrix.


## -parameters




### -param sx [in]

Type: <b>REAL</b>

Real number that specifies the horizontal scaling factor in the scaling matrix. 


### -param sy [in]

Type: <b>REAL</b>

Real number that specifies the vertical scaling factor in the scaling matrix. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of the multiplication. <b>MatrixOrderPrepend</b> specifies that the scaling matrix is on the left, and <b>MatrixOrderAppend</b> specifies that the scaling matrix is on the right. The default value is <b>MatrixOrderPrepend</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/735a9b62-d913-4d06-83bf-86ae093a0dc1">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/b62b1734-119a-4a65-854b-261674a02378">Pen::GetTransform</a>



<a href="https://msdn.microsoft.com/29ea3ff0-0cfa-4f4c-a292-824fdd0705ce">Pen::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/2a473f75-ad8c-4616-98fd-d87946409bb1">Pen::ResetTransform</a>



<a href="https://msdn.microsoft.com/e6a5a579-98a6-43dd-a6b2-882c6a449046">Pen::SetTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

