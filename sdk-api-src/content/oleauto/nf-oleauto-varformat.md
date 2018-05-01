---
UID: NF:oleauto.VarFormat
title: VarFormat function
author: windows-driver-content
description: Formats a variant into string form by parsing a format string.
old-location: automat\varformat.htm
old-project: automat
ms.assetid: 2e1b4fd1-a86b-4933-8934-5d725168a2cd
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: VarFormat, VarFormat function [Automation], _oa96_VarFormat, automat.varformat, oleauto/VarFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
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
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	VarFormat
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# VarFormat function


## -description


Formats a variant into string form by parsing a format string.


## -parameters




### -param pvarIn [in]

The variant.


### -param pstrFormat [in, optional]

The format string. For example "mm-dd-yy".


### -param iFirstDay [in]

First day of the week.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The system default

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Monday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Tuesday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Wednesday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Thursday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Friday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Saturday

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Sunday

</td>
</tr>
</table>
 


### -param iFirstWeek [in]

First week of the year.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The system default.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The first week contains January 1st.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The larger half (four days) of the first week is in the current year.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The first week has seven days.

</td>
</tr>
</table>
 


### -param dwFlags [in]

Flags that control the formatting process. The only flags that can be set are VAR_CALENDAR_HIJRI or VAR_FORMAT_NOSUBSTITUTE.


### -param pbstrOut [out]

The formatted string that represents the variant.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
</table>
 




## -remarks



This function uses the user's default locale while calling <a href="https://msdn.microsoft.com/7cec1bc5-39ea-4b47-880b-62584ff23536">VarTokenizeFormatString</a> and <a href="https://msdn.microsoft.com/36437d1a-970d-4a52-a8a5-1cddfe3d42f3">VarFormatFromTokens</a>.




## -see-also




<a href="https://msdn.microsoft.com/a00ee3c1-9799-4cd8-a13c-063c725aab68">Formatting Routines</a>



<a href="https://msdn.microsoft.com/36437d1a-970d-4a52-a8a5-1cddfe3d42f3">VarFormatFromTokens</a>



<a href="https://msdn.microsoft.com/7cec1bc5-39ea-4b47-880b-62584ff23536">VarTokenizeFormatString</a>
 

 

