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

# ITextPara::GetLineSpacingRule


## -description


Retrieves the line-spacing rule for the text range.


## -parameters




### -param pValue

Type: <b>long*</b>

A variable that is one of the following values to indicate the line-spacing rule. 
					

<a id="tomLineSpaceSingle"></a>
<a id="tomlinespacesingle"></a>
<a id="TOMLINESPACESINGLE"></a>


#### tomLineSpaceSingle

<a id="tomLineSpace1pt5"></a>
<a id="tomlinespace1pt5"></a>
<a id="TOMLINESPACE1PT5"></a>


#### tomLineSpace1pt5

<a id="tomLineSpaceDouble"></a>
<a id="tomlinespacedouble"></a>
<a id="TOMLINESPACEDOUBLE"></a>


#### tomLineSpaceDouble

<a id="tomLineSpaceAtLeast"></a>
<a id="tomlinespaceatleast"></a>
<a id="TOMLINESPACEATLEAST"></a>


#### tomLineSpaceAtLeast

<a id="tomLineSpaceExactly"></a>
<a id="tomlinespaceexactly"></a>
<a id="TOMLINESPACEEXACTLY"></a>


#### tomLineSpaceExactly

<a id="tomLineSpaceMultiple"></a>
<a id="tomlinespacemultiple"></a>
<a id="TOMLINESPACEMULTIPLE"></a>


#### tomLineSpaceMultiple

<a id="tomLineSpacePercent"></a>
<a id="tomlinespacepercent"></a>
<a id="TOMLINESPACEPERCENT"></a>


#### tomLineSpacePercent


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetLineSpacingRule</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b9d3ad53-3d64-4260-b4cf-41038e652ba8">GetLineSpacing</a>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/36ef5af4-90dd-4185-92c9-5c4e88bf5ec2">SetLineSpacing</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

