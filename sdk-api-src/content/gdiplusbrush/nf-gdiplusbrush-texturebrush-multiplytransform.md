---
UID: NF:gdiplusbrush.TextureBrush.MultiplyTransform
title: TextureBrush::MultiplyTransform
author: windows-sdk-content
description: The TextureBrush::MultiplyTransform method updates this brush's transformation matrix with the product of itself and another matrix.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_MultiplyTransform_matrix_order_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\multiplytransform_37matrix_order.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: MultiplyTransform, MultiplyTransform method [GDI+], MultiplyTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],MultiplyTransform method, TextureBrush.MultiplyTransform, TextureBrush::MultiplyTransform, _gdiplus_CLASS_TextureBrush_MultiplyTransform_matrix_order_, gdiplus._gdiplus_CLASS_TextureBrush_MultiplyTransform_matrix_order_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusbrush.h
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
tech.root: 
req.typenames: KnownGamingPrivileges
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - TextureBrush.MultiplyTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# TextureBrush::MultiplyTransform


## -description


The <b>TextureBrush::MultiplyTransform</b> method updates this brush's transformation matrix with the product of itself and another matrix.


## -parameters




### -param matrix [in]

Type: <b><a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to the matrix to be multiplied by this brush's current transformation matrix. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a></b>

Optional. Element of the 
					<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of multiplication. <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a> specifies that the passed matrix is on the left, and <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderAppend</a> specifies that the passed matrix is on the right. The default value is <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/12e1e132-a93f-4438-8a1d-9036a43a8fd8">Filling a Shape with an Image Texture</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a>



<a href="https://msdn.microsoft.com/4fe7b87d-5568-4f1b-82b0-0edef2c7b296">TextureBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/9843531d-7894-4d2f-b9da-b807ae307e4f">TextureBrush::ResetTransform</a>



<a href="https://msdn.microsoft.com/b710bd0f-f1b2-4ab9-b7ef-d790c1f36a04">TextureBrush::RotateTransform</a>



<a href="https://msdn.microsoft.com/00df6637-afc5-411a-a724-ce5d6e0a64ec">TextureBrush::ScaleTransform</a>



<a href="https://msdn.microsoft.com/ba1ecf7c-58ea-4832-b9b2-fce884180805">TextureBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/a414f0f5-0d75-420c-87ae-d83e0b7dfcd4">TextureBrush::TranslateTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

