---
UID: NF:msctf.ITfRangeACP.GetExtent
title: ITfRangeACP::GetExtent (msctf.h)
description: ITfRangeACP::GetExtent method
helpviewer_keywords: ["GetExtent","GetExtent method [Text Services Framework]","GetExtent method [Text Services Framework]","ITfRangeACP interface","ITfRangeACP interface [Text Services Framework]","GetExtent method","ITfRangeACP.GetExtent","ITfRangeACP::GetExtent","_tsf_itfrangeacp_getextent_ref","msctf/ITfRangeACP::GetExtent","tsf.itfrangeacp_getextent"]
old-location: tsf\itfrangeacp_getextent.htm
tech.root: TSF
ms.assetid: 14838cea-1a19-4faa-ac7f-617fde82432d
ms.date: 12/05/2018
ms.keywords: GetExtent, GetExtent method [Text Services Framework], GetExtent method [Text Services Framework],ITfRangeACP interface, ITfRangeACP interface [Text Services Framework],GetExtent method, ITfRangeACP.GetExtent, ITfRangeACP::GetExtent, _tsf_itfrangeacp_getextent_ref, msctf/ITfRangeACP::GetExtent, tsf.itfrangeacp_getextent
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
 - ITfRangeACP::GetExtent
 - msctf/ITfRangeACP::GetExtent
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
 - ITfRangeACP.GetExtent
---

# ITfRangeACP::GetExtent


## -description

Obtains the application character position and length of the range object.

## -parameters

### -param pacpAnchor [out]

Pointer to a <b>LONG</b> value that receives the application character position of the range start anchor.

### -param pcch [out]

Pointer to a <b>LONG</b> value that receives the number of characters in the range.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

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
</table>

## -remarks

This method should only be called by the owner of the ACP-based context because the character position and range length will only have meaning to a caller that recognizes the text store implementation.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfrangeacp">ITfRangeACP</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrangeacp-setextent">ITfRangeACP::SetExtent
      </a>