---
UID: NF:ctffunc.ITfFnReconversion.Reconvert
title: ITfFnReconversion::Reconvert (ctffunc.h)
description: ITfFnReconversion::Reconvert method
helpviewer_keywords: ["ITfFnReconversion interface [Text Services Framework]","Reconvert method","ITfFnReconversion.Reconvert","ITfFnReconversion::Reconvert","Reconvert","Reconvert method [Text Services Framework]","Reconvert method [Text Services Framework]","ITfFnReconversion interface","_tsf_itffnreconversion_reconvert_ref","ctffunc/ITfFnReconversion::Reconvert","tsf.itffnreconversion_reconvert"]
old-location: tsf\itffnreconversion_reconvert.htm
tech.root: TSF
ms.assetid: 81d0f376-c059-4fcf-b85b-645bc98f957d
ms.date: 12/05/2018
ms.keywords: ITfFnReconversion interface [Text Services Framework],Reconvert method, ITfFnReconversion.Reconvert, ITfFnReconversion::Reconvert, Reconvert, Reconvert method [Text Services Framework], Reconvert method [Text Services Framework],ITfFnReconversion interface, _tsf_itffnreconversion_reconvert_ref, ctffunc/ITfFnReconversion::Reconvert, tsf.itffnreconversion_reconvert
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
 - ITfFnReconversion::Reconvert
 - ctffunc/ITfFnReconversion::Reconvert
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
 - ITfFnReconversion.Reconvert
---

# ITfFnReconversion::Reconvert


## -description

Invokes the reconversion process for a range of text.

## -parameters

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that covers the text to be reconverted. To obtain this range object call <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-queryrange">ITfFnReconversion::QueryRange</a>.

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

If this method causes some type of user interface to be displayed, such as a dialog box, this method must not wait for the UI to be dismissed before returning.

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnreconversion">ITfFnReconversion</a>



<a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-queryrange">ITfFnReconversion::QueryRange
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>