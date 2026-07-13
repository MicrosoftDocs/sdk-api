---
UID: NF:recapis.GetUnicodeRanges
title: GetUnicodeRanges function (recapis.h)
description: Returns the ranges of Unicode points that the recognizer supports.
helpviewer_keywords: ["4a354073-e971-43ba-93c9-84fa2e8c59aa","GetUnicodeRanges","GetUnicodeRanges function [Tablet PC]","recapis/GetUnicodeRanges","tablet.getunicoderanges"]
old-location: tablet\getunicoderanges.htm
tech.root: tablet
ms.assetid: 4a354073-e971-43ba-93c9-84fa2e8c59aa
ms.date: 12/05/2018
ms.keywords: 4a354073-e971-43ba-93c9-84fa2e8c59aa, GetUnicodeRanges, GetUnicodeRanges function [Tablet PC], recapis/GetUnicodeRanges, tablet.getunicoderanges
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
 - GetUnicodeRanges
 - recapis/GetUnicodeRanges
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
 - GetUnicodeRanges
---

# GetUnicodeRanges function


## -description

Returns the ranges of Unicode points that the recognizer supports.

## -parameters

### -param hrec

Handle to the recognizer.

### -param pcRanges

On input, the number of ranges the <i>pcr</i> buffer can hold. On output, the number of ranges the <i>pcr</i> buffer contains.

### -param pcr

Array of <a href="/windows/desktop/api/rectypes/ns-rectypes-character_range">CHARACTER_RANGE</a> structures. Each structure contains a range of Unicode points that the recognizer supports. The order of the array is arbitrary. To determine the required size of the buffer, set <i>pcr</i> to <b>NULL</b>; use the number of ranges to allocate the <i>pcr</i> buffer.

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
<dt><b>TPC_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcr</i> buffer is too small.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -remarks

This function is optional.

Some recognizers do not support this capability, but may still include the <b>GetUnicodeRanges Function</b> function. For such recognizers the <b>GetUnicodeRanges</b> function returns E_NOTIMPL.

To control the Unicode ranges used by a specific recognizer context, use the <a href="/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges">GetEnabledUnicodeRanges</a> and <a href="/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges">SetEnabledUnicodeRanges</a> functions. These ranges are constrained to be a subset of the ranges returned by <b>GetUnicodeRanges</b>.

Microsoft gesture recognizers use Unicode characters from 0xF000 to 0xF0FF. Each single Unicode value in this range represents a single gesture. For a complete list of Unicode values for gestures, see <a href="/windows/desktop/tablet/unicode-range-values-of-gestures">Unicode Range Values of Gestures</a>.

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges">GetEnabledUnicodeRanges Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges">SetEnabledUnicodeRanges Function</a>