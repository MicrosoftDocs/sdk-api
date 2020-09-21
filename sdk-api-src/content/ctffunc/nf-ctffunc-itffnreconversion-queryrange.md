---
UID: NF:ctffunc.ITfFnReconversion.QueryRange
title: ITfFnReconversion::QueryRange (ctffunc.h)
description: The ITfFnReconversion::QueryRange method obtains the range of text that the reconversion applies to.
helpviewer_keywords: ["ITfFnReconversion interface [Text Services Framework]","QueryRange method","ITfFnReconversion.QueryRange","ITfFnReconversion::QueryRange","QueryRange","QueryRange method [Text Services Framework]","QueryRange method [Text Services Framework]","ITfFnReconversion interface","_tsf_itffnreconversion_queryrange_ref","ctffunc/ITfFnReconversion::QueryRange","tsf.itffnreconversion_queryrange"]
old-location: tsf\itffnreconversion_queryrange.htm
tech.root: TSF
ms.assetid: 022d0ad7-5359-48df-b83b-2319eb1a84bf
ms.date: 12/05/2018
ms.keywords: ITfFnReconversion interface [Text Services Framework],QueryRange method, ITfFnReconversion.QueryRange, ITfFnReconversion::QueryRange, QueryRange, QueryRange method [Text Services Framework], QueryRange method [Text Services Framework],ITfFnReconversion interface, _tsf_itffnreconversion_queryrange_ref, ctffunc/ITfFnReconversion::QueryRange, tsf.itffnreconversion_queryrange
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
 - ITfFnReconversion::QueryRange
 - ctffunc/ITfFnReconversion::QueryRange
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
 - ITfFnReconversion.QueryRange
---

# ITfFnReconversion::QueryRange


## -description

The <b>ITfFnReconversion::QueryRange</b> method obtains the range of text that the reconversion applies to.

## -parameters

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that covers all or part of the text to be reconverted.

### -param ppNewRange

[in, out] Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> pointer that receives a range object that covers all of text that can be reconverted. If none of the text covered by <i>pRange</i> can be reconverted, this parameters receives NULL. In this case, the method will return S_OK, so the caller must verify that this parameter is not NULL before using the pointer.

When this method is implemented by a text service, this parameter is optional and can be NULL. In this case, the range is not required.

When the TSF manager implementation of this method is called, this parameter is not optional and cannot be NULL.

### -param pfConvertable [out]

Pointer to a <b>BOOL</b> value that receives zero if none of the text covered by <i>pRange</i> can be reconverted or nonzero otherwise.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnreconversion">ITfFnReconversion</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>