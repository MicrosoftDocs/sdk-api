---
UID: NF:recapis.GetBestResultString
title: GetBestResultString function (recapis.h)
description: Retrieves the best result string.
helpviewer_keywords: ["97d60330-c808-4d16-a197-7bad7ca9080e","GetBestResultString","GetBestResultString function [Tablet PC]","recapis/GetBestResultString","tablet.getbestresultstring"]
old-location: tablet\getbestresultstring.htm
tech.root: tablet
ms.assetid: 97d60330-c808-4d16-a197-7bad7ca9080e
ms.date: 12/05/2018
ms.keywords: 97d60330-c808-4d16-a197-7bad7ca9080e, GetBestResultString, GetBestResultString function [Tablet PC], recapis/GetBestResultString, tablet.getbestresultstring
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: inkobjcore.lib
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetBestResultString
 - recapis/GetBestResultString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - GetBestResultString
---

# GetBestResultString function


## -description

Retrieves the best result string.

## -parameters

### -param hrc

Handle to the recognizer context.

### -param pcSize

On input, the number of characters the <i>pwcBestResult</i> buffer can hold. On output, the number of characters the <i>pwcBestResult</i> buffer contains. If <i>pwcBestResult</i> is <b>NULL</b>, the function returns the required size of the buffer that you use to allocate the <i>pwcBestResult</i> buffer.

### -param pwcBestResult

Recognition result. If the buffer is too small, the function truncates the string. The string is not <b>NULL</b>-terminated. To determine the required size of the buffer, set <i>pwcBestResult</i> to <b>NULL</b>; use <i>pcSize</i> to allocate the <i>pwcBestResult</i> buffer.

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

For Latin and East Asian recognizers this result in combination with an empty string in <i>pwcBestResult</i> means that no recognition result exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The string is truncated to fit in the <i>pwcBestResult</i> buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_NOT_RELEVANT</b></dt>
</dl>
</td>
<td width="60%">
The recognizer context does not contain results. 

</td>
</tr>
</table>

