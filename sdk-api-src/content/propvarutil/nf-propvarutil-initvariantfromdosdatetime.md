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

# InitVariantFromDosDateTime function


## -description


Initializes a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure with a date and time given in the format used by Microsoft MS-DOS. The date and time values are converted to the format used to store date and time in a <b>VARIANT</b>.


## -parameters




### -param wDate [in]

Type: <b>WORD</b>

<b>WORD</b> value that represents an MS-DOS date. See <a href="61b029cb-8b60-400a-a6bb-a3f6839dc9d2">DosDateTimeToVariantTime</a> for more information about this format.


### -param wTime [in]

Type: <b>WORD</b>

<b>WORD</b> value that represents an MS-DOS time. See <a href="61b029cb-8b60-400a-a6bb-a3f6839dc9d2">DosDateTimeToVariantTime</a> for more information about this format.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a <b>VT_DATE</b> variant.

See <a href="61b029cb-8b60-400a-a6bb-a3f6839dc9d2">DosDateTimeToVariantTime</a> for more information about the formats of <i>wDate</i>, <i>wTime</i>, and of the resulting variant date.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitVariantFromDosDateTime">InitVariantFromDosDateTime</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// WORD wDate, wTime;
// Assume variables wDate and wTime are initialized and valid.
VARIANT var;

HRESULT hr = InitVariantFromDosDateTime(wDate, wTime, &amp;var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_DATE.
    VariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromFileTime">InitPropVariantFromFileTime</a>



<a href="shell.InitVariantFromFileTime">InitVariantFromFileTime</a>



<a href="shell.VariantToDosDateTime">VariantToDosDateTime</a>



<a href="shell.VariantToFileTime">VariantToFileTime</a>
 

 

