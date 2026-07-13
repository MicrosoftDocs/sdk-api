---
UID: NF:recapis.SetEnabledUnicodeRanges
title: SetEnabledUnicodeRanges function (recapis.h)
description: Enables one or more Unicode point ranges on the context.
helpviewer_keywords: ["68c7c06b-eab1-419d-ad58-22cbd4c3065e","SetEnabledUnicodeRanges","SetEnabledUnicodeRanges function [Tablet PC]","recapis/SetEnabledUnicodeRanges","tablet.setenabledunicoderanges"]
old-location: tablet\setenabledunicoderanges.htm
tech.root: tablet
ms.assetid: 68c7c06b-eab1-419d-ad58-22cbd4c3065e
ms.date: 11/06/2024
ms.keywords: 68c7c06b-eab1-419d-ad58-22cbd4c3065e, SetEnabledUnicodeRanges, SetEnabledUnicodeRanges function [Tablet PC], recapis/SetEnabledUnicodeRanges, tablet.setenabledunicoderanges
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
 - SetEnabledUnicodeRanges
 - recapis/SetEnabledUnicodeRanges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport 
api_location:
 - recapis.h
 - inkobjcore.dll
 - mshwgst.dll
api_name:
 - SetEnabledUnicodeRanges
---

# SetEnabledUnicodeRanges function


## -description

Enables one or more Unicode point ranges on the context.

## -parameters

### -param hrc

The handle to the recognizer context.

### -param cRanges

The number of ranges in the <i>pRanges</i> buffer.

### -param pcr

An array of <a href="/windows/desktop/api/rectypes/ns-rectypes-character_range">CHARACTER_RANGE</a> structures. Each structure identifies a range of Unicode points that you want to enable in the recognizer. The order of the array is arbitrary.

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
<dt><b>TPC_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The recognizer does not support one of the specified Unicode point ranges.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is an invalid pointer.

</td>
</tr>
</table>

## -remarks

The <b>SetEnabledUnicodeRanges</b> function is optional.

Some recognizers do not support enabling and disabling specific code points, but may still include the <b>SetEnabledUnicodeRanges</b> function. For such recognizers, the <b>SetEnabledUnicodeRanges</b> function returns E_NOTIMPL.

Each recognizer supports one or more Unicode point ranges. To determine which Unicode point ranges the recognizer supports, call the <a href="/windows/desktop/api/recapis/nf-recapis-getunicoderanges">GetUnicodeRanges</a> function. If you do not call this function, the recognizer uses a default set of Unicode point ranges. The default ranges are recognizer specific.

The Microsoft gesture recognizer uses Unicode characters from 0xF000 to 0xF0FF. Each single Unicode value in this range represents a single gesture. For a complete list of Unicode values for gestures, see <a href="/windows/desktop/tablet/unicode-range-values-of-gestures">Unicode Range Values of Gestures</a>.

## -see-also

<a href="/windows/desktop/api/rectypes/ns-rectypes-character_range">CHARACTER_RANGE Structure</a>



<a href="/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges">GetEnabledUnicodeRanges Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-getunicoderanges">GetUnicodeRanges Function</a>