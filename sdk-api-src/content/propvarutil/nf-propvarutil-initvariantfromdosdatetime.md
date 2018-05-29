---
UID: NF:propvarutil.InitVariantFromDosDateTime
title: InitVariantFromDosDateTime function
author: windows-sdk-content
description: Initializes a VARIANT structure with a date and time given in the format used by Microsoft MS-DOS. The date and time values are converted to the format used to store date and time in a VARIANT.
old-location: properties\InitVariantFromDosDateTime.htm
old-project: properties
ms.assetid: deb1b3e6-4e7b-49c2-a4dc-e3dfaa2727a0
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: InitVariantFromDosDateTime, InitVariantFromDosDateTime function [Windows Properties], _shell_InitVariantFromDosDateTime, properties.InitVariantFromDosDateTime, propvarutil/InitVariantFromDosDateTime, shell.InitVariantFromDosDateTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Propvarutil.h
api_name:
-	InitVariantFromDosDateTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

