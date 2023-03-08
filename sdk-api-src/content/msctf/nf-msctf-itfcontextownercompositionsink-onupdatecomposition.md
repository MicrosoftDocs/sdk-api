---
UID: NF:msctf.ITfContextOwnerCompositionSink.OnUpdateComposition
title: ITfContextOwnerCompositionSink::OnUpdateComposition (msctf.h)
description: ITfContextOwnerCompositionSink::OnUpdateComposition method
helpviewer_keywords: ["ITfContextOwnerCompositionSink interface [Text Services Framework]","OnUpdateComposition method","ITfContextOwnerCompositionSink.OnUpdateComposition","ITfContextOwnerCompositionSink::OnUpdateComposition","OnUpdateComposition","OnUpdateComposition method [Text Services Framework]","OnUpdateComposition method [Text Services Framework]","ITfContextOwnerCompositionSink interface","_tsf_itfcontextownercompositionsink_onupdatecomposition_ref","msctf/ITfContextOwnerCompositionSink::OnUpdateComposition","tsf.itfcontextownercompositionsink_onupdatecomposition"]
old-location: tsf\itfcontextownercompositionsink_onupdatecomposition.htm
tech.root: TSF
ms.assetid: 18c13a32-918b-4178-a72d-0f7d10c2a68d
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerCompositionSink interface [Text Services Framework],OnUpdateComposition method, ITfContextOwnerCompositionSink.OnUpdateComposition, ITfContextOwnerCompositionSink::OnUpdateComposition, OnUpdateComposition, OnUpdateComposition method [Text Services Framework], OnUpdateComposition method [Text Services Framework],ITfContextOwnerCompositionSink interface, _tsf_itfcontextownercompositionsink_onupdatecomposition_ref, msctf/ITfContextOwnerCompositionSink::OnUpdateComposition, tsf.itfcontextownercompositionsink_onupdatecomposition
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
req.dll: Msimtf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextOwnerCompositionSink::OnUpdateComposition
 - msctf/ITfContextOwnerCompositionSink::OnUpdateComposition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msimtf.dll
api_name:
 - ITfContextOwnerCompositionSink.OnUpdateComposition
---

# ITfContextOwnerCompositionSink::OnUpdateComposition


## -description

Called when an existing composition is changed.

## -parameters

### -param pComposition [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfcompositionview">ITfCompositionView</a> object that represents the composition updated.

### -param pRangeNew [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that contains the range of text the composition will cover after the composition is updated.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To determine what has changed within the composition, compare <i>pRangeNew</i> with the range returned from <a href="/windows/desktop/api/msctf/nf-msctf-itfcompositionview-getrange">ITfCompositionView::GetRange</a>. The range returned by <b>ITfCompositionView::GetRange</b> is not updated until after <b>ITfContextOwnerCompositionSink::OnUpdateComposition</b> returns.

## -see-also

[ITfCompositionView interface](nn-msctf-itfcompositionview.md), [ITfContextOwnerCompositionSink interface](nn-msctf-itfcontextownercompositionsink.md), [ITfCompositionView::GetRange](nf-msctf-itfcompositionview-getrange.md), [ITfRange interface](nn-msctf-itfrange.md)