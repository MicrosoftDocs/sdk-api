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

# ITextPara::GetAlignment


## -description


Retrieves the current paragraph alignment value.


## -parameters




### -param pValue

Type: <b>long*</b>

The paragraph alignment, which can be one of the following values.

<a id="tomAlignLeft"></a>
<a id="tomalignleft"></a>
<a id="TOMALIGNLEFT"></a>


#### tomAlignLeft

<a id="tomAlignCenter"></a>
<a id="tomaligncenter"></a>
<a id="TOMALIGNCENTER"></a>


#### tomAlignCenter

<a id="tomAlignRight"></a>
<a id="tomalignright"></a>
<a id="TOMALIGNRIGHT"></a>


#### tomAlignRight

<a id="tomAlignJustify"></a>
<a id="tomalignjustify"></a>
<a id="TOMALIGNJUSTIFY"></a>


#### tomAlignJustify

<a id="tomAlignInterWord"></a>
<a id="tomaligninterword"></a>
<a id="TOMALIGNINTERWORD"></a>


#### tomAlignInterWord

<a id="tomAlignNewspaper"></a>
<a id="tomalignnewspaper"></a>
<a id="TOMALIGNNEWSPAPER"></a>


#### tomAlignNewspaper

<a id="tomAlignInterLetter"></a>
<a id="tomaligninterletter"></a>
<a id="TOMALIGNINTERLETTER"></a>


#### tomAlignInterLetter

<a id="tomAlignScaled"></a>
<a id="tomalignscaled"></a>
<a id="TOMALIGNSCALED"></a>


#### tomAlignScaled


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetAlignment</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
The <i>pValue</i> parameter is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The paragraph format object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/7d4dbd7e-8164-4005-bcd2-36ddf5fbf9a9">SetAlignment</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

