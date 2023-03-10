---
UID: NF:msctf.ITfCompositionView.GetRange
title: ITfCompositionView::GetRange (msctf.h)
description: ITfCompositionView::GetRange method
helpviewer_keywords: ["GetRange","GetRange method [Text Services Framework]","GetRange method [Text Services Framework]","ITfCompositionView interface","ITfCompositionView interface [Text Services Framework]","GetRange method","ITfCompositionView.GetRange","ITfCompositionView::GetRange","_tsf_itfcompositionview_getrange_ref","msctf/ITfCompositionView::GetRange","tsf.itfcompositionview_getrange"]
old-location: tsf\itfcompositionview_getrange.htm
tech.root: TSF
ms.assetid: 31372688-be81-4883-9fc7-ed3f7b2f7934
ms.date: 12/05/2018
ms.keywords: GetRange, GetRange method [Text Services Framework], GetRange method [Text Services Framework],ITfCompositionView interface, ITfCompositionView interface [Text Services Framework],GetRange method, ITfCompositionView.GetRange, ITfCompositionView::GetRange, _tsf_itfcompositionview_getrange_ref, msctf/ITfCompositionView::GetRange, tsf.itfcompositionview_getrange
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
 - ITfCompositionView::GetRange
 - msctf/ITfCompositionView::GetRange
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
 - ITfCompositionView.GetRange
---

# ITfCompositionView::GetRange


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

[ITfCompositionView interface](nn-msctf-itfcompositionview.md), [ITfRange interface](nn-msctf-itfrange.md)