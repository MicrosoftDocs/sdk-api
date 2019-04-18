---
UID: NF:msinkaut.IInkRecognizerGuide.put_Columns
title: IInkRecognizerGuide::put_Columns (msinkaut.h)
author: windows-sdk-content
description: Gets or sets the number of columns in the recognition guide box.
old-location: tablet\inkrecognizerguide_columns.htm
tech.root: tablet
ms.assetid: dfc2848c-6cd6-4dd6-95b6-4097ef641835
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Columns property [Tablet PC], Columns property [Tablet PC],IInkRecognizerGuide interface, IInkRecognizerGuide interface [Tablet PC],Columns property, IInkRecognizerGuide.Columns, IInkRecognizerGuide.put_Columns, IInkRecognizerGuide::Columns, IInkRecognizerGuide::get_Columns, IInkRecognizerGuide::put_Columns, InkRecognizerGuide.get_Columns, InkRecognizerGuide.put_Columns, dfc2848c-6cd6-4dd6-95b6-4097ef641835, msinkaut/IInkRecognizerGuide::Columns, msinkaut/IInkRecognizerGuide::get_Columns, msinkaut/IInkRecognizerGuide::put_Columns, put_Columns, tablet.inkrecognizerguide_columns
ms.topic: method
req.header: msinkaut.h
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizerGuide.Columns
 - IInkRecognizerGuide.get_Columns
 - IInkRecognizerGuide.put_Columns
 - InkRecognizerGuide.get_Columns
 - InkRecognizerGuide.put_Columns
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognizerGuide::put_Columns


## -description



Gets or sets the number of columns in the recognition guide  box.



This property is read/write.


## -parameters


## -remarks



Column width is determined by the size of the drawn box. To get or set the drawn box, use the <a href="https://msdn.microsoft.com/f99095e1-8e7f-47eb-9234-70f651ebf793">DrawnBox</a> property.

Use the values of <b>Columns</b> and <a href="https://msdn.microsoft.com/5b1204ca-40b0-4752-8294-6f94412e8e7c">Rows</a> to control the kind of recognition input that you use. When <b>Columns</b> and <b>Rows</b> are both greater than zero, boxed input is used. The following table lists potential input modes and which values to set the <b>Columns</b> and <b>Rows</b> properties for each mode.

<table>
<tr>
<th>For this type of input</th>
<th>Set the <a href="https://msdn.microsoft.com/5b1204ca-40b0-4752-8294-6f94412e8e7c">Rows</a> property to</th>
<th>And set the <b>Columns</b> property to</th>
</tr>
<tr>
<td>
Free input

</td>
<td>
0

</td>
<td>
0

</td>
</tr>
<tr>
<td>
Vertical Lined input with 1 line

</td>
<td>
0

</td>
<td>
1

</td>
</tr>
<tr>
<td>
Vertical Lined input with n lines

</td>
<td>
0

</td>
<td>
n

</td>
</tr>
<tr>
<td>
Horizontal Lined input with 1 line

</td>
<td>
1

</td>
<td>
0

</td>
</tr>
<tr>
<td>
Horizontal Lined input with n lines

</td>
<td>
n

</td>
<td>
0

</td>
</tr>
<tr>
<td>
Boxed input with 1 box

</td>
<td>
1

</td>
<td>
1

</td>
</tr>
<tr>
<td>
Boxed input in a horizontal line with n boxes

</td>
<td>
n

</td>
<td>
1

</td>
</tr>
<tr>
<td>
Boxed input in a grid of boxes x rows by z columns

</td>
<td>
x

</td>
<td>
z

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f99095e1-8e7f-47eb-9234-70f651ebf793">DrawnBox Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846802(v=VS.85).aspx">IInkRecognizerGuide</a>



<a href="https://msdn.microsoft.com/c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7">InkRecognizerGuide Class</a>



<a href="https://msdn.microsoft.com/5b1204ca-40b0-4752-8294-6f94412e8e7c">Rows Property</a>
 

 

