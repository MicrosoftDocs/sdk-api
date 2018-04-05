---
UID: NF:d2d1svg.SetAttributeValue
title: SetAttributeValue function
author: windows-driver-content
description: Sets an attribute of this element.
old-location: direct2d\id2d1svgelement_setattributevalue_overload.htm
old-project: Direct2D
ms.assetid: 33403a07-28d1-4138-ea7f-04f3ac42a8f7
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: SetAttributeValue, SetAttributeValue methods [Direct2D], d2d1svg/SetAttributeValue, direct2d.id2d1svgelement_setattributevalue_overload
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1svg.h
req.include-header: 
req.target-type: Windows
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
req.typenames: D2D1_SVG_VISIBILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d2d1svg.h
api_name:
-	ID2D1SvgElement::SetAttributeValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# SetAttributeValue function


## -description


<span>Sets an attribute of this element.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FC7AF14F-16B3-498F-A2E3-F8ACF836DAAC">SetAttributeValue(PCWSTR, FLOAT)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element using a float.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/652A0C00-59BC-41E7-8B9D-F4AE37416610">SetAttributeValue(PCWSTR, D2D1_COLOR_F &)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element as a color.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49EFE20B-4122-4426-9A47-7572696A59A2">SetAttributeValue(PCWSTR, D2D1_FILL_MODE)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element as a fill mode. This method can be used to set the value of the 'fill-rule' or 'clip-rule' properties.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7B5828F9-F69D-4346-A2EB-5D00AD08B46F">SetAttributeValue(PCWSTR, D2D1_SVG_DISPLAY)</a>
</td>
<td align="left" width="63%">
Gets an attribute of this element as a display value. This method can be used to get the value of the display property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18FD0ECC-1045-4914-9461-999952B4EAAF">SetAttributeValue(PCWSTR, D2D1_EXTEND_MODE)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element as an extend mode value. This method can be used to set the value of a spreadMethod attribute.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C8D942A4-EBE7-433E-9B2F-2432A1305861">SetAttributeValue(PCWSTR, D2D1_SVG_OVERFLOW)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element as an overflow value. This method can be used to set the value of the overflow property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5348071B-36B7-40B7-8CF2-A7C185D30510">SetAttributeValue(PCWSTR, D2D1_SVG_LINE_CAP)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element as a line cap value. This method can be used to set the value of the stroke-linecap property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61C6D9AC-09F7-4F42-B476-88D32EB167C4">SetAttributeValue(PCWSTR, D2D1_SVG_LENGTH &)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element as a length value.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B559FC14-8B16-4272-A83F-6F8C0CC2D438">SetAttributeValue(PCWSTR, D2D1_SVG_LINE_JOIN)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element as a line join value. This method can be used to set the value of the stroke-linejoin property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/330FCA46-C799-478C-9687-3D407D121ACB">SetAttributeValue(PCWSTR, D2D1_SVG_UNIT_TYPE)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element as a unit type value. This method can be used to set the value of a gradientUnits or clipPathUnits attribute.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1E4AAA78-6746-4DD8-8BD8-C1AB63A51A9B">SetAttributeValue(PCWSTR, ID2D1SvgAttribute *)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element using an interface.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/860407EC-1736-4AE6-A8AA-40E475C6520B">SetAttributeValue(PCWSTR, D2D1_SVG_VISIBILITY)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element as a visibility value. This method can be used to set the value of the visibility property.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98CDD40C-C39B-41B9-8978-9C9B480DB3C4">SetAttributeValue(PCWSTR, D2D1_MATRIX_3X2_F &)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element as a matrix value. This method can be used to set the value of a transform or gradientTransform attribute.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F95B714E-309B-4E6D-99C9-331FB476EC59">SetAttributeValue(PCWSTR, D2D1_SVG_PRESERVE_ASPECT_RATIO &)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element as a preserve aspect ratio value. This method can be used to set the value of a preserveAspectRatio attribute.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56796F1B-5DC2-4E9C-A80E-40EA791E6784">SetAttributeValue(PCWSTR, D2D1_SVG_ATTRIBUTE_STRING_TYPE, PCWSTR)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element using a string. 

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ACAA04E-8ABB-49D1-A6F8-BCCEAD1DA460">SetAttributeValue(PCWSTR, D2D1_SVG_ATTRIBUTE_POD_TYPE , void *, UINT32)</a>
</td>
<td align="left" width="63%">
Sets an attribute of this element using a POD type.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://msdn.microsoft.com/19099DC9-EA14-41C5-A9DF-5EBB12696C79">ID2D1SvgElement</a>
 

 

