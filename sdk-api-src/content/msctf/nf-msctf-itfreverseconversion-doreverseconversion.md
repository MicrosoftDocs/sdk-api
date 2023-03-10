---
UID: NF:msctf.ITfReverseConversion.DoReverseConversion
title: ITfReverseConversion::DoReverseConversion (msctf.h)
description: Performs a reverse conversion of the specified string.
helpviewer_keywords: ["DoReverseConversion","DoReverseConversion method [Text Services Framework]","DoReverseConversion method [Text Services Framework]","ITfReverseConversion interface","ITfReverseConversion interface [Text Services Framework]","DoReverseConversion method","ITfReverseConversion.DoReverseConversion","ITfReverseConversion::DoReverseConversion","msctf/ITfReverseConversion::DoReverseConversion","tsf.itfreverseconversion__doreverseconversion"]
old-location: tsf\itfreverseconversion__doreverseconversion.htm
tech.root: TSF
ms.assetid: a2312cd4-316a-42a6-85a5-e5ef819faa79
ms.date: 12/05/2018
ms.keywords: DoReverseConversion, DoReverseConversion method [Text Services Framework], DoReverseConversion method [Text Services Framework],ITfReverseConversion interface, ITfReverseConversion interface [Text Services Framework],DoReverseConversion method, ITfReverseConversion.DoReverseConversion, ITfReverseConversion::DoReverseConversion, msctf/ITfReverseConversion::DoReverseConversion, tsf.itfreverseconversion__doreverseconversion
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfReverseConversion::DoReverseConversion
 - msctf/ITfReverseConversion::DoReverseConversion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfReverseConversion.DoReverseConversion
---

# ITfReverseConversion::DoReverseConversion


## -description

<p class="CCE_Message">[<b>DoReverseConversion</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.]

Performs a reverse conversion of the specified string.

## -parameters

### -param lpstr [in]

The string to convert.

### -param ppList [out]

 The result of the conversion: a list of the key strokes required to create the string specified by <i>lpstr</i>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The conversion result is stored in <i>ppList</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The conversion result, <i>ppList</i>, contains no entries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_FAIL</dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

A reverse conversion provides the keystroke sequences required to create the specified string.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfreverseconversion">ITfReverseConversion</a>