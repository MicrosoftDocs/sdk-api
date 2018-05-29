---
UID: NF:gdipluspen.Pen.MultiplyTransform
title: Pen::MultiplyTransform
author: windows-sdk-content
description: The Pen::MultiplyTransform method updates the world transformation matrix of this Pen object with the product of itself and another matrix.
old-location: gdiplus\_gdiplus_CLASS_Pen_MultiplyTransform_matrix_order_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\multiplytransform_75matrix_order.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: MultiplyTransform, MultiplyTransform method [GDI+], MultiplyTransform method [GDI+],Pen class, Pen class [GDI+],MultiplyTransform method, Pen.MultiplyTransform, Pen::MultiplyTransform, _gdiplus_CLASS_Pen_MultiplyTransform_matrix_order_, gdiplus._gdiplus_CLASS_Pen_MultiplyTransform_matrix_order_
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WmfPlaceableFileHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Pen.MultiplyTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Pen::MultiplyTransform


## -description


The <b>Pen::MultiplyTransform</b> method updates the world transformation matrix of this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object with the product of itself and another matrix.


## -parameters




### -param matrix [in]

Type: <b><a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that is multiplied with the world transformation matrix of this 
					<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of the multiplication. <b>MatrixOrderPrepend</b> specifies that the passed matrix is on the left, and <b>MatrixOrderAppend</b> specifies that the passed matrix is on the right. The default value is <b>MatrixOrderPrepend</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/735a9b62-d913-4d06-83bf-86ae093a0dc1">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/b62b1734-119a-4a65-854b-261674a02378">Pen::GetTransform</a>



<a href="https://msdn.microsoft.com/2a473f75-ad8c-4616-98fd-d87946409bb1">Pen::ResetTransform</a>



<a href="https://msdn.microsoft.com/c88b622c-3c9d-4640-96f5-0bccddd6f412">Pen::RotateTransform</a>



<a href="https://msdn.microsoft.com/0605fcdb-bb04-46dd-8818-9d524a1d90d1">Pen::ScaleTransform</a>



<a href="https://msdn.microsoft.com/e6a5a579-98a6-43dd-a6b2-882c6a449046">Pen::SetTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

