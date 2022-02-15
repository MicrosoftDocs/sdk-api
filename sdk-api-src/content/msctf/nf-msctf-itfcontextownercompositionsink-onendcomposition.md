---
UID: NF:msctf.ITfContextOwnerCompositionSink.OnEndComposition
title: ITfContextOwnerCompositionSink::OnEndComposition (msctf.h)
description: ITfContextOwnerCompositionSink::OnEndComposition method
helpviewer_keywords: ["ITfContextOwnerCompositionSink interface [Text Services Framework]","OnEndComposition method","ITfContextOwnerCompositionSink.OnEndComposition","ITfContextOwnerCompositionSink::OnEndComposition","OnEndComposition","OnEndComposition method [Text Services Framework]","OnEndComposition method [Text Services Framework]","ITfContextOwnerCompositionSink interface","_tsf_itfcontextownercompositionsink_onendcomposition_ref","msctf/ITfContextOwnerCompositionSink::OnEndComposition","tsf.itfcontextownercompositionsink_onendcomposition"]
old-location: tsf\itfcontextownercompositionsink_onendcomposition.htm
tech.root: TSF
ms.assetid: 816aaa81-1b51-4e01-b49c-a9cbe2b87735
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerCompositionSink interface [Text Services Framework],OnEndComposition method, ITfContextOwnerCompositionSink.OnEndComposition, ITfContextOwnerCompositionSink::OnEndComposition, OnEndComposition, OnEndComposition method [Text Services Framework], OnEndComposition method [Text Services Framework],ITfContextOwnerCompositionSink interface, _tsf_itfcontextownercompositionsink_onendcomposition_ref, msctf/ITfContextOwnerCompositionSink::OnEndComposition, tsf.itfcontextownercompositionsink_onendcomposition
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
 - ITfContextOwnerCompositionSink::OnEndComposition
 - msctf/ITfContextOwnerCompositionSink::OnEndComposition
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
 - ITfContextOwnerCompositionSink.OnEndComposition
---

# ITfContextOwnerCompositionSink::OnEndComposition


## -description

Called when a composition is terminated.

## -parameters

### -param pComposition [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfcompositionview">ITfCompositionView</a> object that represents the composition terminated.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

[ITfCompositionView interface](nn-msctf-itfcompositionview.md), [ITfContextOwnerCompositionSink interface](nn-msctf-itfcontextownercompositionsink.md)