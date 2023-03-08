---
UID: NF:msctf.ITfCompositionSink.OnCompositionTerminated
title: ITfCompositionSink::OnCompositionTerminated (msctf.h)
description: ITfCompositionSink::OnCompositionTerminated method
helpviewer_keywords: ["ITfCompositionSink interface [Text Services Framework]","OnCompositionTerminated method","ITfCompositionSink.OnCompositionTerminated","ITfCompositionSink::OnCompositionTerminated","OnCompositionTerminated","OnCompositionTerminated method [Text Services Framework]","OnCompositionTerminated method [Text Services Framework]","ITfCompositionSink interface","_tsf_itfcompositionsink_oncompositionterminated_ref","msctf/ITfCompositionSink::OnCompositionTerminated","tsf.itfcompositionsink_oncompositionterminated"]
old-location: tsf\itfcompositionsink_oncompositionterminated.htm
tech.root: TSF
ms.assetid: 4b7c3993-6d01-492f-9bb5-241a1cbd4b63
ms.date: 12/05/2018
ms.keywords: ITfCompositionSink interface [Text Services Framework],OnCompositionTerminated method, ITfCompositionSink.OnCompositionTerminated, ITfCompositionSink::OnCompositionTerminated, OnCompositionTerminated, OnCompositionTerminated method [Text Services Framework], OnCompositionTerminated method [Text Services Framework],ITfCompositionSink interface, _tsf_itfcompositionsink_oncompositionterminated_ref, msctf/ITfCompositionSink::OnCompositionTerminated, tsf.itfcompositionsink_oncompositionterminated
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
req.dll: Imekrcic.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCompositionSink::OnCompositionTerminated
 - msctf/ITfCompositionSink::OnCompositionTerminated
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfCompositionSink.OnCompositionTerminated
---

# ITfCompositionSink::OnCompositionTerminated


## -description

Called when a composition is terminated.

## -parameters

### -param ecWrite [in]

Contains a <a href="/windows/desktop/TSF/tfeditcookie">TfEditCookie</a> value that identifies the edit context. This is the same value passed for <i>ecWrite</i> in the call to <a href="/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition">ITfContextComposition::StartComposition</a>.

### -param pComposition [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfcomposition">ITfComposition</a> object terminated.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

There is no required action for the TSF text service when this method is called. The TSF text service can use this notification to revert partially composed text into readable text or erase the composition entirely. The TSF manager will automatically clear the GUID_PROP_COMPOSING property value over the affected text.

## -see-also

[ITfComposition interface](nn-msctf-itfcomposition.md), [ITfCompositionSink interface](nn-msctf-itfcompositionsink.md), [ITfContextComposition::StartComposition](nf-msctf-itfcontextcomposition-startcomposition.md), [TfEditCookie](/windows/desktop/TSF/tfeditcookie)