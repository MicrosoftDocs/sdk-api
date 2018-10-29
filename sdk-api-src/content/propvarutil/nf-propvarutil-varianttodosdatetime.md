---
UID: NF:propvarutil.VariantToDosDateTime
title: VariantToDosDateTime function
author: windows-sdk-content
description: Extracts a date and time value in Microsoft MS-DOS format from a VARIANT structure.
old-location: properties\VariantToDosDateTime.htm
tech.root: properties
ms.assetid: ebbba4d9-8e97-422d-b52f-67c417f295cc
ms.author: windowssdkdev
ms.date: 10/19/2018
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
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantToDosDateTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# VariantToDosDateTime function


## -description


Extracts a date and time value in Microsoft MS-DOS format from a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure.


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



This helper function is used when the calling application expects a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> to hold a datetime value.

If the source <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> is of type <b>VT_DATE</b>, this function extracts the datetime value.

If the source <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> is not of type <b>VT_DATE</b>, the function attempts to convert the value in the <b>VARIANT</b> structure into the right format. If a conversion is not possible, <a href="https://msdn.microsoft.com/en-us/library/Bb776597(v=VS.85).aspx">VariantToDosDateTime</a> returns a failure code. See <a href="https://msdn.microsoft.com/en-us/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a> for a list of possible conversions.

See <a href="https://msdn.microsoft.com/en-us/library/ms221238(v=VS.85).aspx">DosDateTimeToVariantTime</a> for more information about the formats of <i>pwDate</i>, <i>pwTime</i>, and the source datetime value.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776597(v=VS.85).aspx">VariantToDosDateTime</a> to access a datetime value in a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a>.

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




<a href="https://msdn.microsoft.com/en-us/library/Bb762320(v=VS.85).aspx">InitVariantFromDosDateTime</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776542(v=VS.85).aspx">PropVariantToFileTime</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776602(v=VS.85).aspx">VariantToFileTime</a>
 

 

