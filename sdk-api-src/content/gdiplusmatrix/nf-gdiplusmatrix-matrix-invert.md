---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# Matrix::Invert


## -description


If this matrix is invertible, the <b>Matrix::Invert</b> method replaces the elements of this matrix with the elements of its inverse.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



If this matrix is not invertible, the method fails and returns InvalidParameter.


#### Examples



The following example passes the address of a 
						<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object to the 
						<a href="https://msdn.microsoft.com/458b62ad-04f0-4202-92db-b1fcf43b3ffa">SetTransform</a> method of a 
						<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object and then draws a rectangle. The rectangle is translated 30 units right and 20 units down by the world transformation of the 
						<b>Graphics</b> object. The code calls the <b>Matrix::Invert</b> method of the 
						<b>Matrix</b> object and sets the world transformation of the 
						<b>Graphics</b> object to the inverted matrix. The code draws a second rectangle that is translated 30 units left and 20 units up.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_Invert(HDC hdc)
{
   Graphics myGraphics(hdc);
   Pen myPen(Color(255, 0, 0, 255));

   Matrix matrix(1.0f, 0.0f, 0.0f, 1.0f, 30.0f, 20.0f);

   myGraphics.SetTransform(&amp;matrix);
   myGraphics.DrawRectangle(&amp;myPen, 0, 0, 200, 100);
   matrix.Invert();
   myGraphics.SetTransform(&amp;matrix);
   myGraphics.DrawRectangle(&amp;myPen, 0, 0, 200, 100);  
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9f744c2a-f1f3-4a7e-ab0c-37aa1df01623">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/7104f46b-3a3d-4185-9369-cfd89864de61">Matrix::IsInvertible</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

