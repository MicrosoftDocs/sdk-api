---
UID: NF:oleauto.VarFormatFromTokens
title: VarFormatFromTokens function
author: windows-driver-content
description: Takes a tokenized format string and applies it to a variant to produce a formatted output string.
old-location: automat\varformatfromtokens.htm
old-project: automat
ms.assetid: 36437d1a-970d-4a52-a8a5-1cddfe3d42f3
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: VarFormatFromTokens, VarFormatFromTokens function [Automation], _oa96_VarFormatFromTokens, automat.varformatfromtokens, oleauto/VarFormatFromTokens
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
-	VarFormatFromTokens
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# VarFormatFromTokens function


## -description


Takes a tokenized format string and applies it to a variant to produce a formatted output string.


## -parameters




### -param pvarIn [in]

The variant containing the value to format.


### -param pstrFormat [in, optional]

The original format string.


### -param pbTokCur [in]

The tokenized format string from <a href="https://msdn.microsoft.com/7cec1bc5-39ea-4b47-880b-62584ff23536">VarTokenizeFormatString</a>.


### -param dwFlags [in]

The only flags that can be set are VAR_CALENDAR_HIJRI or VAR_FORMAT_NOSUBSTITUTE.


### -param pbstrOut [out]

The formatted output string.


### -param lcid [in]

The locale to use for the formatted output string.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.


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
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The argument could not be coerced to the specified type.


</td>
</tr>
</table>
 




## -remarks



The locale <i>lcid</i> controls the formatted output string.




