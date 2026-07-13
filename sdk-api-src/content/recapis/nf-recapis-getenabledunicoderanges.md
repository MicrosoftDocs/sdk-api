---
UID: NF:recapis.GetEnabledUnicodeRanges
title: GetEnabledUnicodeRanges function (recapis.h)
description: Retrieves a list of Unicode point ranges enabled on the context. If you do not call the SetEnabledUnicodeRanges function to specify the enabled ranges, this function returns the recognizer's default Unicode point ranges.
helpviewer_keywords: ["047a72f9-a627-4c8b-b271-13d3c873abc9","GetEnabledUnicodeRanges","GetEnabledUnicodeRanges function [Tablet PC]","recapis/GetEnabledUnicodeRanges","tablet.getenabledunicoderanges"]
old-location: tablet\getenabledunicoderanges.htm
tech.root: tablet
ms.assetid: 047a72f9-a627-4c8b-b271-13d3c873abc9
ms.date: 12/05/2018
ms.keywords: 047a72f9-a627-4c8b-b271-13d3c873abc9, GetEnabledUnicodeRanges, GetEnabledUnicodeRanges function [Tablet PC], recapis/GetEnabledUnicodeRanges, tablet.getenabledunicoderanges
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
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
req.lib: 
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetEnabledUnicodeRanges
 - recapis/GetEnabledUnicodeRanges
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
 - GetEnabledUnicodeRanges
---

# GetEnabledUnicodeRanges function


## -description

Retrieves a list of Unicode point ranges enabled on the context. If you do not call the <a href="/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges">SetEnabledUnicodeRanges</a> function to specify the enabled ranges, this function returns the recognizer's default Unicode point ranges.

## -parameters

### -param hrc

The handle to the recognizer context.

### -param pcRanges

On input, the number of <a href="/windows/desktop/api/rectypes/ns-rectypes-character_range">CHARACTER_RANGE</a> structures the <i>pcr</i> buffer can contain. On output, the number of ranges the <i>pcr</i> buffer contains.

### -param pcr

An array of CHARACTER_RANGE structures. Each structure contains a range of Unicode points enabled on the context. The order of the array is arbitrary. To determine the size of the buffer, set <i>pcr</i> to <b>NULL</b>; use the number of ranges to allocate the <i>pcr</i> buffer.

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

Some recognizers do not support enabling and disabling specific Unicode points, but may still include the <b>GetEnabledUnicodeRanges</b> function. For such recognizers the <b>GetEnabledUnicodeRanges</b> function returns the same ranges as the <a href="/windows/desktop/api/recapis/nf-recapis-getunicoderanges">GetUnicodeRanges</a> function.

Microsoft gesture recognizers use Unicode characters from 0xF000 to 0xF0FF. Each single Unicode value in this range represents a single gesture. For a complete list of Unicode values for gestures, see <a href="/windows/desktop/tablet/unicode-range-values-of-gestures">Unicode Range Values of Gestures</a>.

## -see-also

<a href="/windows/desktop/api/rectypes/ns-rectypes-character_range">CHARACTER_RANGE Structure</a>



<a href="/windows/desktop/api/recapis/nf-recapis-getunicoderanges">GetUnicodeRanges Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges">SetEnabledUnicodeRanges Function</a>