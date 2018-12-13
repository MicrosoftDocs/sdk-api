---
UID: NF:gdiplustypes.PointF.operator-sub
title: PointF::operator-sub
author: windows-sdk-content
description: The PointF::operator- method subtracts the X and Y data members of two PointF objects.
old-location: gdiplus\_gdiplus_CLASS_PointF_operator_opminus_point_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pointfclass\pointfmethods\operator_17point.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PointF class [GDI+],operator- method, PointF.operator-, PointF.operator-(const PointF&), PointF.operator-sub, PointF::operator-, PointF::operator-sub, _gdiplus_CLASS_PointF_operator_opminus_point_, gdiplus._gdiplus_CLASS_PointF_operator_opminus_point_, operator-, operator- method [GDI+], operator- method [GDI+],PointF class
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplustypes.h
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
 - PointF.operator-
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PointF::operator-sub


## -description


The <b>PointF::operator-</b> method subtracts the <b>X</b> and <b>Y</b> data members of two <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> objects.


## -parameters




### -param point [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a></b>

Reference to a <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> object whose <b>X</b> and <b>Y</b> data members are subtracted from the <b>X</b> and <b>Y</b> data members of this <b>PointF</b> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a></b>
</strong>

This method returns a <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> object that is the difference of two <b>PointF</b> objects.




## -remarks



This method overloads the subtraction operator for <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> objects. If A, B, and C are <b>PointF</b> objects, the statement <b>C = A - B</b> is equivalent to <b>C = A.operator-(B)</b>.


#### Examples



The following example creates two <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> objects, then subtracts the second <b>PointF</b> object from the first <b>PointF</b> object and stores the result in a third <b>PointF</b> object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PointF point1(40.0f, 10.0f);
PointF point2(-20.0f, -30.0f);

// Point3 now contains the coordinates (60.0f, 40.0f).
PointF point3 = point1 - point2; </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535007(v=VS.85).aspx">Equals</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535008(v=VS.85).aspx">operator+</a>
 

 

