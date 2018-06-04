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

# Rect::IsEmptyArea


## -description


The <b>Rect::IsEmptyArea</b> method determines whether this rectangle is empty.


## -parameters






## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the rectangle is empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



A rectangle is defined as empty if either the width or the height is zero or less.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">Rect</a> object, inflates the dimensions of the rectangle, and determines whether the rectangle is empty.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_IsEmptyArea(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Rect object, and inflate the dimensions.
   Rect rect(50, 50, 200, 100);
   rect.Inflate(0, -120);

   // Determine whether the rectangle is empty.
   if(rect.IsEmptyArea())

   // The rectangle does not enclose any area.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4875dec3-e57e-4109-8c63-c3dc4db6080d">Inflate Methods</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">Rect</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

