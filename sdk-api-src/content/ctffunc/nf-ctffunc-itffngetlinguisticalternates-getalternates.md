---
UID: NF:ctffunc.ITfFnGetLinguisticAlternates.GetAlternates
title: ITfFnGetLinguisticAlternates::GetAlternates (ctffunc.h)
description: Returns a list of alternate strings for a given text range.
helpviewer_keywords: ["GetAlternates","GetAlternates method [Text Services Framework]","GetAlternates method [Text Services Framework]","ITfFnGetLinguisticAlternates interface","ITfFnGetLinguisticAlternates interface [Text Services Framework]","GetAlternates method","ITfFnGetLinguisticAlternates.GetAlternates","ITfFnGetLinguisticAlternates::GetAlternates","ctffunc/ITfFnGetLinguisticAlternates::GetAlternates","tsf.itffngetlinguisticalternates_getalternates"]
old-location: tsf\itffngetlinguisticalternates_getalternates.htm
tech.root: TSF
ms.assetid: 17BB0DF8-3F97-423C-A2FD-CDC7590EE49B
ms.date: 12/05/2018
ms.keywords: GetAlternates, GetAlternates method [Text Services Framework], GetAlternates method [Text Services Framework],ITfFnGetLinguisticAlternates interface, ITfFnGetLinguisticAlternates interface [Text Services Framework],GetAlternates method, ITfFnGetLinguisticAlternates.GetAlternates, ITfFnGetLinguisticAlternates::GetAlternates, ctffunc/ITfFnGetLinguisticAlternates::GetAlternates, tsf.itffngetlinguisticalternates_getalternates
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfFnGetLinguisticAlternates::GetAlternates
 - ctffunc/ITfFnGetLinguisticAlternates::GetAlternates
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctffunc.h
api_name:
 - ITfFnGetLinguisticAlternates.GetAlternates
---

# ITfFnGetLinguisticAlternates::GetAlternates


## -description

Returns a list of alternate strings for a given text range.

## -parameters

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that covers the text to return alternates for.

### -param ppCandidateList [out]

Pointer to an <a href="/windows/desktop/api/ctffunc/nn-ctffunc-itfcandidatelist">ITfCandidateList</a> pointer that receives the list object containing alternate strings.

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
An unspecified error occurred or no alternates could be generated for the range. *<i>ppCandidateList</i> is returned as null.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffngetlinguisticalternates">ITfFnGetLinguisticAlternates</a>