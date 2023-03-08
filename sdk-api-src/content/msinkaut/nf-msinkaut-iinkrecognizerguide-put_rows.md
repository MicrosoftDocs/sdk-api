---
UID: NF:msinkaut.IInkRecognizerGuide.put_Rows
title: IInkRecognizerGuide::put_Rows (msinkaut.h)
description: Gets or sets the number of rows in the recognition guide. (Put)
helpviewer_keywords: ["5b1204ca-40b0-4752-8294-6f94412e8e7c","IInkRecognizerGuide interface [Tablet PC]","Rows property","IInkRecognizerGuide.Rows","IInkRecognizerGuide.put_Rows","IInkRecognizerGuide::Rows","IInkRecognizerGuide::get_Rows","IInkRecognizerGuide::put_Rows","InkRecognizerGuide.get_Rows","InkRecognizerGuide.put_Rows","Rows property [Tablet PC]","Rows property [Tablet PC]","IInkRecognizerGuide interface","get_Rows","msinkaut/IInkRecognizerGuide::Rows","msinkaut/IInkRecognizerGuide::get_Rows","msinkaut/IInkRecognizerGuide::put_Rows","put_Rows","tablet.inkrecognizerguide_rows"]
old-location: tablet\inkrecognizerguide_rows.htm
tech.root: tablet
ms.assetid: 5b1204ca-40b0-4752-8294-6f94412e8e7c
ms.date: 12/05/2018
ms.keywords: 5b1204ca-40b0-4752-8294-6f94412e8e7c, IInkRecognizerGuide interface [Tablet PC],Rows property, IInkRecognizerGuide.Rows, IInkRecognizerGuide.put_Rows, IInkRecognizerGuide::Rows, IInkRecognizerGuide::get_Rows, IInkRecognizerGuide::put_Rows, InkRecognizerGuide.get_Rows, InkRecognizerGuide.put_Rows, Rows property [Tablet PC], Rows property [Tablet PC],IInkRecognizerGuide interface, get_Rows, msinkaut/IInkRecognizerGuide::Rows, msinkaut/IInkRecognizerGuide::get_Rows, msinkaut/IInkRecognizerGuide::put_Rows, put_Rows, tablet.inkrecognizerguide_rows
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkRecognizerGuide::put_Rows
 - msinkaut/IInkRecognizerGuide::put_Rows
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizerGuide.Rows
 - IInkRecognizerGuide.get_Rows
 - IInkRecognizerGuide.put_Rows
 - InkRecognizerGuide.get_Rows
 - InkRecognizerGuide.put_Rows
---

# IInkRecognizerGuide::put_Rows


## -description

Gets or sets the number of rows in the recognition guide.



This property is read/write.

## -parameters

## -remarks

Row height is determined by the size of the drawn box. To get or set the drawn box, use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox">DrawnBox</a> property.

Use the values of the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns">Columns</a> and <b>Rows</b> properties to control the kind of recognition input that you use. When the <b>Columns</b> and <b>Rows</b> properties are both greater than zero, boxed input is used. The following table lists potential input modes and which values to set the <b>Columns</b> and <b>Rows</b> properties for each mode.

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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns">Columns Property</a>



<a href="../msinkaut/nn-msinkaut-iinkrecognizerguide.md">IInkRecognizerGuide</a>



<a href="/windows/desktop/tablet/inkrecognizerguide-class">InkRecognizerGuide Class</a>
