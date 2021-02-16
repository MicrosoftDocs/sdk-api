---
UID: NF:ctffunc.ITfFnLMProcessor.QueryRange
title: ITfFnLMProcessor::QueryRange (ctffunc.h)
description: ITfFnLMProcessor::QueryRange method
helpviewer_keywords: ["ITfFnLMProcessor interface [Text Services Framework]","QueryRange method","ITfFnLMProcessor.QueryRange","ITfFnLMProcessor::QueryRange","QueryRange","QueryRange method [Text Services Framework]","QueryRange method [Text Services Framework]","ITfFnLMProcessor interface","_tsf_itffnlmprocessor_queryrange_ref","ctffunc/ITfFnLMProcessor::QueryRange","tsf.itffnlmprocessor_queryrange"]
old-location: tsf\itffnlmprocessor_queryrange.htm
tech.root: TSF
ms.assetid: 84a9bf73-7215-429a-9573-66acf4d3ff18
ms.date: 12/05/2018
ms.keywords: ITfFnLMProcessor interface [Text Services Framework],QueryRange method, ITfFnLMProcessor.QueryRange, ITfFnLMProcessor::QueryRange, QueryRange, QueryRange method [Text Services Framework], QueryRange method [Text Services Framework],ITfFnLMProcessor interface, _tsf_itffnlmprocessor_queryrange_ref, ctffunc/ITfFnLMProcessor::QueryRange, tsf.itffnlmprocessor_queryrange
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITfFnLMProcessor::QueryRange
 - ctffunc/ITfFnLMProcessor::QueryRange
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
 - ITfFnLMProcessor.QueryRange
---

# ITfFnLMProcessor::QueryRange


## -description

Obtains the range of text that a reconversion applies to.

## -parameters

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that covers all or part of the text to be reconverted.

### -param ppNewRange [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> pointer that receives a range object that covers all of the text that can be reconverted. If none of the text covered by <i>pRange</i> can be reconverted, this parameters receives <b>NULL</b>. In this case, the method will return S_OK; the caller must verify that this parameter is not <b>NULL</b> before using the pointer.

This parameter is optional and can be <b>NULL</b>. In this case, the range is not required.

### -param pfAccepted [out]

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

## -remarks

This method is identical to <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-queryrange">ITfFnReconversion::QueryRange</a>. When <b>ITfFnReconversion::QueryRange</b> is called in the text service, the text service should forward the call to this method if a language model processor is installed. If no language model processor is installed, the text service should perform its default processing.

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnlmprocessor">ITfFnLMProcessor</a>



<a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-queryrange">ITfFnReconversion::QueryRange</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>