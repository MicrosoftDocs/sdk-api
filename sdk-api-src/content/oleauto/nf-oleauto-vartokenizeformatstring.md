---
UID: NF:oleauto.VarTokenizeFormatString
title: VarTokenizeFormatString function (oleauto.h)
description: Parses the actual format string into a series of tokens which can be used to format variants using VarFormatFromTokens.
helpviewer_keywords: ["VarTokenizeFormatString","VarTokenizeFormatString function [Automation]","_oa96_VarTokenizeFormatString","automat.vartokenizeformatstring","oleauto/VarTokenizeFormatString"]
old-location: automat\vartokenizeformatstring.htm
tech.root: automat
ms.assetid: 7cec1bc5-39ea-4b47-880b-62584ff23536
ms.date: 12/05/2018
ms.keywords: VarTokenizeFormatString, VarTokenizeFormatString function [Automation], _oa96_VarTokenizeFormatString, automat.vartokenizeformatstring, oleauto/VarTokenizeFormatString
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VarTokenizeFormatString
 - oleauto/VarTokenizeFormatString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarTokenizeFormatString
---

# VarTokenizeFormatString function


## -description

Parses the actual format string into a series of tokens which can be used to format variants using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-varformatfromtokens">VarFormatFromTokens</a>.

## -parameters

### -param pstrFormat [in, optional]

The format string. For example "mm-dd-yy".

### -param rgbTok [in, out]

The destination token buffer.

### -param cbTok [in]

The size of the destination token buffer.

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

### -param lcid [in]

The locale to interpret format string in.

### -param pcbActual [in, optional]

Points to the integer which is set to the first generated token. This parameter can be NULL.

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
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BUFFERTOOSMALL
</b></dt>
</dl>
</td>
<td width="60%">
The destination token buffer is too small.

</td>
</tr>
</table>

## -remarks

Parsing the format string once and then using it repeatedly is usually faster than calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-varformat">VarFormat</a> repeatedly, because the latter routine calls <b>VarTokenizeFormatString</b> for each call.

The locale you pass in controls how the format string is interpreted, not how the actual output of <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-varformatfromtokens">VarFormatFromTokens</a> looks.