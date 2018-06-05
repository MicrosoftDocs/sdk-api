---
UID: NF:gdiplusgraphics.Graphics.MultiplyTransform
title: Graphics::MultiplyTransform
author: windows-sdk-content
description: The Graphics::MultiplyTransform method updates this Graphics object's world transformation matrix with the product of itself and another matrix.
old-location: gdiplus\_gdiplus_CLASS_Graphics_MultiplyTransform_matrix_order_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\multiplytransform.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Graphics class [GDI+],MultiplyTransform method, Graphics.MultiplyTransform, Graphics::MultiplyTransform, MultiplyTransform, MultiplyTransform method [GDI+], MultiplyTransform method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_MultiplyTransform_matrix_order_, gdiplus._gdiplus_CLASS_Graphics_MultiplyTransform_matrix_order_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusgraphics.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Graphics.MultiplyTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::MultiplyTransform


## -description


The <b>Graphics::MultiplyTransform</b> method updates this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object's world transformation matrix with the product of itself and another matrix.


## -parameters




### -param matrix [in]

Type: <b><a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a matrix that will be multiplied by the world transformation matrix of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of multiplication. MatrixOrderPrepend specifies that the passed matrix is on the left, and MatrixOrderAppend specifies that the passed matrix is on the right. The default value is MatrixOrderPrepend. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/735a9b62-d913-4d06-83bf-86ae093a0dc1">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/f5f1a7bb-4f17-4865-b26e-8672ae78c3a7">Graphics::GetTransform</a>



<a href="https://msdn.microsoft.com/10357224-cfbd-4d02-af94-93cdff80d466">Graphics::ResetTransform</a>



<a href="https://msdn.microsoft.com/554cd11e-9b22-48c5-a823-bd29f879fba7">Graphics::RotateTransform</a>



<a href="https://msdn.microsoft.com/040bfd10-1a2b-4277-9d27-0919d9efe371">Graphics::ScaleTransform</a>



<a href="https://msdn.microsoft.com/458b62ad-04f0-4202-92db-b1fcf43b3ffa">Graphics::SetTransform</a>



<a href="https://msdn.microsoft.com/d9c29b36-8f21-4d0b-99c7-5e7d635ee1a1">Graphics::TransformPoints</a>



<a href="https://msdn.microsoft.com/99b51fb7-b1de-421f-9743-bf6a5ec758ef">Graphics::TranslateTransform</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

