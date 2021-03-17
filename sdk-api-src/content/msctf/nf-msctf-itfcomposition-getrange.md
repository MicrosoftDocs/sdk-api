---
UID: NF:msctf.ITfComposition.GetRange
title: ITfComposition::GetRange (msctf.h)
description: ITfComposition::GetRange method
helpviewer_keywords: ["GetRange","GetRange method [Text Services Framework]","GetRange method [Text Services Framework]","ITfComposition interface","ITfComposition interface [Text Services Framework]","GetRange method","ITfComposition.GetRange","ITfComposition::GetRange","_tsf_itfcomposition_getrange_ref","msctf/ITfComposition::GetRange","tsf.itfcomposition_getrange"]
old-location: tsf\itfcomposition_getrange.htm
tech.root: TSF
ms.assetid: 14a726c3-6531-4d49-9f22-20460be02b81
ms.date: 12/05/2018
ms.keywords: GetRange, GetRange method [Text Services Framework], GetRange method [Text Services Framework],ITfComposition interface, ITfComposition interface [Text Services Framework],GetRange method, ITfComposition.GetRange, ITfComposition::GetRange, _tsf_itfcomposition_getrange_ref, msctf/ITfComposition::GetRange, tsf.itfcomposition_getrange
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfComposition::GetRange
 - msctf/ITfComposition::GetRange
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
 - ITfComposition.GetRange
---

# ITfComposition::GetRange


## -description

Obtains a range object that contains the text covered by the composition.

## -parameters

### -param ppRange [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfcomposition">ITfRange</a> interface pointer that receives the range object. It is possible that the range will have zero length.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

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
<i>ppRange</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The composition has already terminated.

</td>
</tr>
</table>

## -see-also

[ITfComposition interface](nn-msctf-itfcomposition.md), [ITfRange interface](nn-msctf-itfrange.md)