---
UID: NF:ctffunc.ITfFnPlayBack.QueryRange
title: ITfFnPlayBack::QueryRange (ctffunc.h)
description: ITfFnPlayBack::QueryRange method
helpviewer_keywords: ["ITfFnPlayBack interface [Text Services Framework]","QueryRange method","ITfFnPlayBack.QueryRange","ITfFnPlayBack::QueryRange","QueryRange","QueryRange method [Text Services Framework]","QueryRange method [Text Services Framework]","ITfFnPlayBack interface","_tsf_itffnplayback_queryrange_ref","ctffunc/ITfFnPlayBack::QueryRange","tsf.itffnplayback_queryrange"]
old-location: tsf\itffnplayback_queryrange.htm
tech.root: TSF
ms.assetid: d6113703-5515-4f1a-8e2e-1373077dafc2
ms.date: 12/05/2018
ms.keywords: ITfFnPlayBack interface [Text Services Framework],QueryRange method, ITfFnPlayBack.QueryRange, ITfFnPlayBack::QueryRange, QueryRange, QueryRange method [Text Services Framework], QueryRange method [Text Services Framework],ITfFnPlayBack interface, _tsf_itffnplayback_queryrange_ref, ctffunc/ITfFnPlayBack::QueryRange, tsf.itffnplayback_queryrange
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
 - ITfFnPlayBack::QueryRange
 - ctffunc/ITfFnPlayBack::QueryRange
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
 - ITfFnPlayBack.QueryRange
---

# ITfFnPlayBack::QueryRange


## -description

Obtains the range of text for a word or phrase that contains audio data.

## -parameters

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that covers all or part of the text that contains audio data.

### -param ppNewRange [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> pointer that receives a range object that covers all of the text that contains audio data. If there is no audio data for the text covered by <i>pRange</i>, this parameters receives <b>NULL</b>. In this case, the method returns S_OK, so the caller must verify that this parameter is not <b>NULL</b> before using the pointer.

### -param pfPlayable [out]

Pointer to a <b>BOOL</b> that receives zero if none of the text covered by <i>pRange</i> has any audio data or nonzero otherwise.

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

The current implementation of this method is simple. It clones <i>pRange</i>, places the clone in <i>ppNewRange</i>, sets <i>pfPlayable</i> to <b>TRUE</b> and returns S_OK.

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnplayback">ITfFnPlayBack</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>