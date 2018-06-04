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

# IInkRecognizerGuide::put_Rows


## -description



Gets or sets the number of rows in the recognition guide.



This property is read/write.


## -parameters


## -remarks



Row height is determined by the size of the drawn box. To get or set the drawn box, use the <a href="https://msdn.microsoft.com/f99095e1-8e7f-47eb-9234-70f651ebf793">DrawnBox</a> property.

Use the values of the <a href="https://msdn.microsoft.com/dfc2848c-6cd6-4dd6-95b6-4097ef641835">Columns</a> and <b>Rows</b> properties to control the kind of recognition input that you use. When the <b>Columns</b> and <b>Rows</b> properties are both greater than zero, boxed input is used. The following table lists potential input modes and which values to set the <b>Columns</b> and <b>Rows</b> properties for each mode.

<table>
<tr>
<th>For this type of input</th>
<th>Set Rows equal to</th>
<th>Set Columns equal to</th>
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
Boxed input in a grid of boxes x rows by y columns

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




<a href="https://msdn.microsoft.com/dfc2848c-6cd6-4dd6-95b6-4097ef641835">Columns Property</a>



<a href="tablet.iinkrecognizerguide">IInkRecognizerGuide</a>



<a href="https://msdn.microsoft.com/c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7">InkRecognizerGuide Class</a>
 

 

