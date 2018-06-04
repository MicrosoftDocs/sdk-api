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

# ITextPara::GetLineSpacing


## -description


Retrieves the line-spacing value for the text range.


## -parameters




### -param pValue

Type: <b>float*</b>

The line-spacing value. The following table shows how this value is interpreted for the different line-spacing rules. 
					

<table class="clsStd">
<tr>
<th>Line spacing rule</th>
<th>Meaning</th>
</tr>
<tr>
<td>tomLineSpaceSingle</td>
<td>The line-spacing value is ignored. </td>
</tr>
<tr>
<td>tomLineSpace1pt5</td>
<td>The line-spacing value is ignored. </td>
</tr>
<tr>
<td>tomLineSpaceDouble</td>
<td>The line-spacing value is ignored. </td>
</tr>
<tr>
<td>tomLineSpaceAtLeast</td>
<td>The line-spacing value specifies the spacing, in floating-point points, from one line to the next. However, if the value is less than single spacing, the control displays single-spaced text.</td>
</tr>
<tr>
<td>tomLineSpaceExactly</td>
<td>The line-spacing value specifies the exact spacing, in floating-point points, from one line to the next (even if the value is less than single spacing).</td>
</tr>
<tr>
<td>tomLineSpaceMultiple</td>
<td>The line-spacing value specifies the line spacing, in lines.</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetLineSpacing</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Value</b></dt>
</dl>
</td>
<td width="60%">
Meaning

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The paragraph formatting object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -remarks



To retrieve the line-spacing rule, call the <a href="https://msdn.microsoft.com/65a1b836-4f90-4b9b-8adc-68ace163df6a">ITextPara::GetLineSpacingRule</a> method.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/65a1b836-4f90-4b9b-8adc-68ace163df6a">GetLineSpacingRule</a>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/36ef5af4-90dd-4185-92c9-5c4e88bf5ec2">SetLineSpacing</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

