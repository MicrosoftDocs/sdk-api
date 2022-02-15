---
UID: NF:msctf.ITfCleanupContextDurationSink.OnEndCleanupContext
title: ITfCleanupContextDurationSink::OnEndCleanupContext (msctf.h)
description: ITfCleanupContextDurationSink::OnEndCleanupContext method
helpviewer_keywords: ["ITfCleanupContextDurationSink interface [Text Services Framework]","OnEndCleanupContext method","ITfCleanupContextDurationSink.OnEndCleanupContext","ITfCleanupContextDurationSink::OnEndCleanupContext","OnEndCleanupContext","OnEndCleanupContext method [Text Services Framework]","OnEndCleanupContext method [Text Services Framework]","ITfCleanupContextDurationSink interface","_tsf_itfcleanupcontextdurationsink_onendcleanupcontext_ref","msctf/ITfCleanupContextDurationSink::OnEndCleanupContext","tsf.itfcleanupcontextdurationsink_onendcleanupcontext"]
old-location: tsf\itfcleanupcontextdurationsink_onendcleanupcontext.htm
tech.root: TSF
ms.assetid: d7af4584-9c77-40cd-a83d-7b6fd3945b17
ms.date: 12/05/2018
ms.keywords: ITfCleanupContextDurationSink interface [Text Services Framework],OnEndCleanupContext method, ITfCleanupContextDurationSink.OnEndCleanupContext, ITfCleanupContextDurationSink::OnEndCleanupContext, OnEndCleanupContext, OnEndCleanupContext method [Text Services Framework], OnEndCleanupContext method [Text Services Framework],ITfCleanupContextDurationSink interface, _tsf_itfcleanupcontextdurationsink_onendcleanupcontext_ref, msctf/ITfCleanupContextDurationSink::OnEndCleanupContext, tsf.itfcleanupcontextdurationsink_onendcleanupcontext
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITfCleanupContextDurationSink::OnEndCleanupContext
 - msctf/ITfCleanupContextDurationSink::OnEndCleanupContext
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
 - ITfCleanupContextDurationSink.OnEndCleanupContext
---

# ITfCleanupContextDurationSink::OnEndCleanupContext


## -description

Called when a context cleanup operation completes.



## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

A context cleanup occurs when:

- The text service is deactivated while a context is still on the context stack. This can occur when the active text service is changed or when the active language changes while the text service is active.
- [ITfThreadMgr::Deactivate](nf-msctf-itfthreadmgr-deactivate.md) is called while a context is still on the context stack.

[ITfCleanupContextDurationSink::OnStartCleanupContext](nf-msctf-itfcleanupcontextdurationsink-onstartcleanupcontext.md) is called just before the TSF manager begins making [ITfCleanupContextSink::OnCleanupContext](nf-msctf-itfcleanupcontextsink-oncleanupcontext.md) notifications. When all of the OnCleanupContext notifications complete, the TSF manager calls **OnEndCleanupContext**.

## -see-also

[ITfCleanupContextDurationSink interface](nn-msctf-itfcleanupcontextdurationsink.md), [ITfCleanupContextDurationSink::OnStartCleanupContext](nf-msctf-itfcleanupcontextdurationsink-onstartcleanupcontext.md), [ITfCleanupContextSink::OnCleanupContext](nf-msctf-itfcleanupcontextsink-oncleanupcontext.md)

