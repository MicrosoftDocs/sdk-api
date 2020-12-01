---
UID: NF:ctffunc.ITfFnLMProcessor.GetReconversion
title: ITfFnLMProcessor::GetReconversion (ctffunc.h)
description: ITfFnLMProcessor::GetReconversion method
helpviewer_keywords: ["GetReconversion","GetReconversion method [Text Services Framework]","GetReconversion method [Text Services Framework]","ITfFnLMProcessor interface","ITfFnLMProcessor interface [Text Services Framework]","GetReconversion method","ITfFnLMProcessor.GetReconversion","ITfFnLMProcessor::GetReconversion","_tsf_itffnlmprocessor_getreconversion_ref","ctffunc/ITfFnLMProcessor::GetReconversion","tsf.itffnlmprocessor_getreconversion"]
old-location: tsf\itffnlmprocessor_getreconversion.htm
tech.root: TSF
ms.assetid: 21fcef3f-252c-4f67-a789-4527b8ee1b94
ms.date: 12/05/2018
ms.keywords: GetReconversion, GetReconversion method [Text Services Framework], GetReconversion method [Text Services Framework],ITfFnLMProcessor interface, ITfFnLMProcessor interface [Text Services Framework],GetReconversion method, ITfFnLMProcessor.GetReconversion, ITfFnLMProcessor::GetReconversion, _tsf_itffnlmprocessor_getreconversion_ref, ctffunc/ITfFnLMProcessor::GetReconversion, tsf.itffnlmprocessor_getreconversion
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
 - ITfFnLMProcessor::GetReconversion
 - ctffunc/ITfFnLMProcessor::GetReconversion
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
 - ITfFnLMProcessor.GetReconversion
---

# ITfFnLMProcessor::GetReconversion


## -description

Obtains an ITfCandidateList object for a range from the language model text service.

## -parameters

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that covers the text to be reconverted. To obtain this range object, call <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-queryrange">ITfFnReconversion::QueryRange</a>.

### -param ppCandList [out]

Pointer to an <b>ITfCandidateList</b> pointer that receives the candidate list object.

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

This method is identical to <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-getreconversion">ITfFnReconversion::GetReconversion</a>. When <b>ITfFnReconversion::GetReconversion</b> is called in the text service, the text service should forward the call to this method if a language model processor is installed. If no language model processor is installed, the text service should perform its default processing.

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itfcandidatelist">ITfCandidateList
      </a>



<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnlmprocessor">ITfFnLMProcessor</a>



<a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-getreconversion">ITfFnReconversion::GetReconversion
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>