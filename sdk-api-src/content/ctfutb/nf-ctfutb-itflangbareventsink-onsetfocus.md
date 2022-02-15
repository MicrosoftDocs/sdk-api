---
UID: NF:ctfutb.ITfLangBarEventSink.OnSetFocus
title: ITfLangBarEventSink::OnSetFocus (ctfutb.h)
description: ITfLangBarEventSink::OnSetFocus method
helpviewer_keywords: ["ITfLangBarEventSink interface [Text Services Framework]","OnSetFocus method","ITfLangBarEventSink.OnSetFocus","ITfLangBarEventSink::OnSetFocus","OnSetFocus","OnSetFocus method [Text Services Framework]","OnSetFocus method [Text Services Framework]","ITfLangBarEventSink interface","_tsf_itflangbareventsink_onsetfocus_ref","ctfutb/ITfLangBarEventSink::OnSetFocus","tsf.itflangbareventsink_onsetfocus"]
old-location: tsf\itflangbareventsink_onsetfocus.htm
tech.root: TSF
ms.assetid: 66d70ff3-dcd4-42cd-bda4-7dbdf1c99da5
ms.date: 12/05/2018
ms.keywords: ITfLangBarEventSink interface [Text Services Framework],OnSetFocus method, ITfLangBarEventSink.OnSetFocus, ITfLangBarEventSink::OnSetFocus, OnSetFocus, OnSetFocus method [Text Services Framework], OnSetFocus method [Text Services Framework],ITfLangBarEventSink interface, _tsf_itflangbareventsink_onsetfocus_ref, ctfutb/ITfLangBarEventSink::OnSetFocus, tsf.itflangbareventsink_onsetfocus
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
 - ITfLangBarEventSink::OnSetFocus
 - ctfutb/ITfLangBarEventSink::OnSetFocus
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
 - ITfLangBarEventSink.OnSetFocus
---

# ITfLangBarEventSink::OnSetFocus


## -description

Called when the thread the event sink was installed from receives the input focus.

## -parameters

### -param dwThreadId [in]

Contains the current thread identifier. This is the same value returned from <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid">GetCurrentThreadId</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid">GetCurrentThreadId</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbareventsink">ITfLangBarEventSink</a>