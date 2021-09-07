---
UID: NF:ctfutb.ITfLangBarEventSink.OnThreadItemChange
title: ITfLangBarEventSink::OnThreadItemChange (ctfutb.h)
description: ITfLangBarEventSink::OnThreadItemChange method
helpviewer_keywords: ["ITfLangBarEventSink interface [Text Services Framework]","OnThreadItemChange method","ITfLangBarEventSink.OnThreadItemChange","ITfLangBarEventSink::OnThreadItemChange","OnThreadItemChange","OnThreadItemChange method [Text Services Framework]","OnThreadItemChange method [Text Services Framework]","ITfLangBarEventSink interface","_tsf_itflangbareventsink_onthreaditemchange_ref","ctfutb/ITfLangBarEventSink::OnThreadItemChange","tsf.itflangbareventsink_onthreaditemchange"]
old-location: tsf\itflangbareventsink_onthreaditemchange.htm
tech.root: TSF
ms.assetid: b59688f9-feb0-4598-bf4a-b0661dda5fad
ms.date: 12/05/2018
ms.keywords: ITfLangBarEventSink interface [Text Services Framework],OnThreadItemChange method, ITfLangBarEventSink.OnThreadItemChange, ITfLangBarEventSink::OnThreadItemChange, OnThreadItemChange, OnThreadItemChange method [Text Services Framework], OnThreadItemChange method [Text Services Framework],ITfLangBarEventSink interface, _tsf_itflangbareventsink_onthreaditemchange_ref, ctfutb/ITfLangBarEventSink::OnThreadItemChange, tsf.itflangbareventsink_onthreaditemchange
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msutb.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfLangBarEventSink::OnThreadItemChange
 - ctfutb/ITfLangBarEventSink::OnThreadItemChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msutb.dll
api_name:
 - ITfLangBarEventSink.OnThreadItemChange
---

# ITfLangBarEventSink::OnThreadItemChange


## -description

Called when a language bar item changes.

## -parameters

### -param dwThreadId [in]

Contains the current thread identifier. This is the same value returned from <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid">GetCurrentThreadId</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid">GetCurrentThreadId</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbareventsink">ITfLangBarEventSink</a>