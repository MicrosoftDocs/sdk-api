---
UID: NF:oleauto.VarFormatDateTime
title: VarFormatDateTime function
author: windows-sdk-content
description: Formats a variant containing named date and time information into a string.
old-location: automat\varformatdatetime.htm
tech.root: automat
ms.assetid: ae97d984-fc08-4e4d-a711-9ceb38aebe1e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: VarFormatDateTime, VarFormatDateTime function [Automation], _oa96_VarFormatDateTime, automat.varformatdatetime, oleauto/VarFormatDateTime
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarFormatDateTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VarFormatDateTime function


## -description


Formats a variant containing named date and time information into a string.


## -parameters




### -param pvarIn [in]

The variant containing the value to format.


### -param iNamedFormat [in]

The named date formats are as follows.

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
General date

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Long date

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Short date

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Long time

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Short time

</td>
</tr>
</table>
 


### -param dwFlags [in]

VAR_CALENDAR_HIJRI is the only flag that can be set.


### -param pbstrOut [out]

Receives the formatted string that represents the variant.


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
 

 

