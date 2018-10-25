---
UID: NF:gdipluspen.Pen.ResetTransform
title: Pen::ResetTransform
author: windows-sdk-content
description: The Pen::ResetTransform method sets the world transformation matrix of this Pen object to the identity matrix.
old-location: gdiplus\_gdiplus_CLASS_Pen_ResetTransform_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\resettransform_27.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Pen class [GDI+],ResetTransform method, Pen.ResetTransform, Pen::ResetTransform, ResetTransform, ResetTransform method [GDI+], ResetTransform method [GDI+],Pen class, _gdiplus_CLASS_Pen_ResetTransform_, gdiplus._gdiplus_CLASS_Pen_ResetTransform_
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
 - Pen.ResetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::ResetTransform


## -description


The <b>Pen::ResetTransform</b> method sets the world transformation matrix of this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object to the identity matrix.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<b>Ok</b> enumeration.




## -remarks



The identity matrix represents a transformation that does nothing. If the world transformation matrix of a 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object is the identity matrix, then no world transformation is applied to items drawn using that 
				<b>Pen</b> object.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object, sets a scaling matrix to the pen, and draws a rectangle. The code then resets the transformation of the pen and draws a second rectangle.


```cpp
VOID Example_ResetTrans(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a pen, and set its transformation.
   Pen pen(Color(255, 0, 0, 255), 2);
   pen.ScaleTransform(8, 4);

   // Draw a rectangle with the transformed pen.
   graphics.DrawRectangle(&pen, 50, 50, 150, 100);

   pen.ResetTransform();

   // Draw a rectangle with no pen transformation.
   graphics.DrawRectangle(&pen, 250, 50, 150, 100);
}
```





## -see-also




<a href="https://msdn.microsoft.com/735a9b62-d913-4d06-83bf-86ae093a0dc1">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/b62b1734-119a-4a65-854b-261674a02378">Pen::GetTransform</a>



<a href="https://msdn.microsoft.com/29ea3ff0-0cfa-4f4c-a292-824fdd0705ce">Pen::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/c88b622c-3c9d-4640-96f5-0bccddd6f412">Pen::RotateTransform</a>



<a href="https://msdn.microsoft.com/0605fcdb-bb04-46dd-8818-9d524a1d90d1">Pen::ScaleTransform</a>



<a href="https://msdn.microsoft.com/e6a5a579-98a6-43dd-a6b2-882c6a449046">Pen::SetTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

