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

# ITextFont::GetUnderline


## -description


Gets the

			type of underlining for the characters in a range.


## -parameters




### -param pValue

Type: <b>long*</b>

The type of underlining. It can be one of the following values. 
					
				

<a id="tomNone"></a>
<a id="tomnone"></a>
<a id="TOMNONE"></a>


#### tomNone

<a id="tomSingle"></a>
<a id="tomsingle"></a>
<a id="TOMSINGLE"></a>


#### tomSingle

<a id="tomWords"></a>
<a id="tomwords"></a>
<a id="TOMWORDS"></a>


#### tomWords

<a id="tomDouble"></a>
<a id="tomdouble"></a>
<a id="TOMDOUBLE"></a>


#### tomDouble

<a id="tomDotted"></a>
<a id="tomdotted"></a>
<a id="TOMDOTTED"></a>


#### tomDotted

<a id="tomDash"></a>
<a id="tomdash"></a>
<a id="TOMDASH"></a>


#### tomDash

<a id="tomDashDot"></a>
<a id="tomdashdot"></a>
<a id="TOMDASHDOT"></a>


#### tomDashDot

<a id="tomDashDotDot"></a>
<a id="tomdashdotdot"></a>
<a id="TOMDASHDOTDOT"></a>


#### tomDashDotDot

<a id="tomWave"></a>
<a id="tomwave"></a>
<a id="TOMWAVE"></a>


#### tomWave

<a id="tomThick"></a>
<a id="tomthick"></a>
<a id="TOMTHICK"></a>


#### tomThick

<a id="tomHair"></a>
<a id="tomhair"></a>
<a id="TOMHAIR"></a>


#### tomHair

<a id="tomDoubleWave"></a>
<a id="tomdoublewave"></a>
<a id="TOMDOUBLEWAVE"></a>


#### tomDoubleWave

<a id="tomHeavyWave"></a>
<a id="tomheavywave"></a>
<a id="TOMHEAVYWAVE"></a>


#### tomHeavyWave

<a id="tomLongDash"></a>
<a id="tomlongdash"></a>
<a id="TOMLONGDASH"></a>


#### tomLongDash

<a id="tomThickDash"></a>
<a id="tomthickdash"></a>
<a id="TOMTHICKDASH"></a>


#### tomThickDash

<a id="tomThickDashDot"></a>
<a id="tomthickdashdot"></a>
<a id="TOMTHICKDASHDOT"></a>


#### tomThickDashDot

<a id="tomThickDashDotDot"></a>
<a id="tomthickdashdotdot"></a>
<a id="TOMTHICKDASHDOTDOT"></a>


#### tomThickDashDotDot

<a id="tomThickDotted"></a>
<a id="tomthickdotted"></a>
<a id="TOMTHICKDOTTED"></a>


#### tomThickDotted

<a id="tomThickLongDash"></a>
<a id="tomthicklongdash"></a>
<a id="TOMTHICKLONGDASH"></a>


#### tomThickLongDash


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
The font object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a58baee4-6264-49ed-bd2c-15ce22cdba94">SetUnderline</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

