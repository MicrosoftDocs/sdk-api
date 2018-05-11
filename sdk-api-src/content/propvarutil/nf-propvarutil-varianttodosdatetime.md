---
UID: NF:propvarutil.VariantToDosDateTime
title: VariantToDosDateTime function
author: windows-driver-content
description: Extracts a date and time value in Microsoft MS-DOS format from a VARIANT structure.
old-location: properties\VariantToDosDateTime.htm
old-project: properties
ms.assetid: ebbba4d9-8e97-422d-b52f-67c417f295cc
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: VariantToDosDateTime, VariantToDosDateTime function [Windows Properties], _shell_VariantToDosDateTime, properties.VariantToDosDateTime, propvarutil/VariantToDosDateTime, shell.VariantToDosDateTime
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	VariantToDosDateTime
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# VariantToDosDateTime function


## -description


Extracts a date and time value in Microsoft MS-DOS format from a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


### -param pwDate [out]

Type: <b>WORD*</b>

When this function returns, contains the extracted <b>WORD</b> that represents a MS-DOS date.


### -param pwTime [out]

Type: <b>WORD*</b>

When this function returns, contains the extracted contains the extracted <b>WORD</b> that represents a MS-DOS time.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used when the calling application expects a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> to hold a datetime value.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is of type <b>VT_DATE</b>, this function extracts the datetime value.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is not of type <b>VT_DATE</b>, the function attempts to convert the value in the <b>VARIANT</b> structure into the right format. If a conversion is not possible, <a href="shell.VariantToDosDateTime">VariantToDosDateTime</a> returns a failure code. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions.

See <a href="61b029cb-8b60-400a-a6bb-a3f6839dc9d2">DosDateTimeToVariantTime</a> for more information about the formats of <i>pwDate</i>, <i>pwTime</i>, and the source datetime value.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.VariantToDosDateTime">VariantToDosDateTime</a> to access a datetime value in a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// VARIANT var;
// Assume variable var is initialize and valid.
// The application expects var to hold a VT_DATE value.

WORD wDate;
WORD wTime;

HRESULT hr = VariantToDosDateTime(var, &amp;wDate, &amp;wTime);

if (SUCCEEDED(hr))
{
    // wDate and wTime are now valid.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitVariantFromDosDateTime">InitVariantFromDosDateTime</a>



<a href="shell.PropVariantChangeType">PropVariantChangeType</a>



<a href="shell.PropVariantToFileTime">PropVariantToFileTime</a>



<a href="shell.VariantToFileTime">VariantToFileTime</a>
 

 

