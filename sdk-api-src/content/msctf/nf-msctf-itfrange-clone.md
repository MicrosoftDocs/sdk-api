---
UID: NF:msctf.ITfRange.Clone
title: ITfRange::Clone (msctf.h)
description: The ITfRange::Clone method duplicates this range of text.
helpviewer_keywords: ["Clone","Clone method [Text Services Framework]","Clone method [Text Services Framework]","ITfRange interface","ITfRange interface [Text Services Framework]","Clone method","ITfRange.Clone","ITfRange::Clone","_tsf_itfrange_clone_ref","msctf/ITfRange::Clone","tsf.itfrange_clone"]
old-location: tsf\itfrange_clone.htm
tech.root: TSF
ms.assetid: 2b85012f-b090-4c91-b29c-b2470ff63ab6
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],ITfRange interface, ITfRange interface [Text Services Framework],Clone method, ITfRange.Clone, ITfRange::Clone, _tsf_itfrange_clone_ref, msctf/ITfRange::Clone, tsf.itfrange_clone
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
 - ITfRange::Clone
 - msctf/ITfRange::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfRange.Clone
---

# ITfRange::Clone


## -description

The <b>ITfRange::Clone</b> method duplicates this range of text.

## -parameters

### -param ppClone [out]

Pointer to a new range object that references this range.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to generate a pointer to the new range.

</td>
</tr>
</table>

## -remarks

The resulting new range object can be modified without affecting the original. However, modifying the document that contains the new range might cause the original range's anchors to be repositioned.

The gravity of the original is preserved in the new range.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/TSF/ranges">Ranges</a>



<a href="/windows/desktop/TSF/text-stores">Text Stores</a>