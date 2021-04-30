---
UID: NF:ctffunc.ITfFnReconversion.GetReconversion
title: ITfFnReconversion::GetReconversion (ctffunc.h)
description: ITfFnReconversion::GetReconversion method
helpviewer_keywords: ["GetReconversion","GetReconversion method [Text Services Framework]","GetReconversion method [Text Services Framework]","ITfFnReconversion interface","ITfFnReconversion interface [Text Services Framework]","GetReconversion method","ITfFnReconversion.GetReconversion","ITfFnReconversion::GetReconversion","_tsf_itffnreconversion_getreconversion_ref","ctffunc/ITfFnReconversion::GetReconversion","tsf.itffnreconversion_getreconversion"]
old-location: tsf\itffnreconversion_getreconversion.htm
tech.root: TSF
ms.assetid: ed696088-c599-4c83-968e-d09d9ae81c10
ms.date: 12/05/2018
ms.keywords: GetReconversion, GetReconversion method [Text Services Framework], GetReconversion method [Text Services Framework],ITfFnReconversion interface, ITfFnReconversion interface [Text Services Framework],GetReconversion method, ITfFnReconversion.GetReconversion, ITfFnReconversion::GetReconversion, _tsf_itffnreconversion_getreconversion_ref, ctffunc/ITfFnReconversion::GetReconversion, tsf.itffnreconversion_getreconversion
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
 - ITfFnReconversion::GetReconversion
 - ctffunc/ITfFnReconversion::GetReconversion
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
 - ITfFnReconversion.GetReconversion
---

# ITfFnReconversion::GetReconversion


## -description

Obtains an ITfCandidateList object for a range of text.

## -parameters

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that covers the text to be reconverted. This range object is obtained by calling <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-queryrange">ITfFnReconversion::QueryRange</a>.

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

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itfcandidatelist">ITfCandidateList
      </a>



<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnreconversion">ITfFnReconversion</a>



<a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-queryrange">ITfFnReconversion::QueryRange
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>