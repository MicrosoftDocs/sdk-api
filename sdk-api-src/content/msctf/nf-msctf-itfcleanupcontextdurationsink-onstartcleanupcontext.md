---
UID: NF:msctf.ITfCleanupContextDurationSink.OnStartCleanupContext
title: ITfCleanupContextDurationSink::OnStartCleanupContext (msctf.h)
description: ITfCleanupContextDurationSink::OnStartCleanupContext method
helpviewer_keywords: ["ITfCleanupContextDurationSink interface [Text Services Framework]","OnStartCleanupContext method","ITfCleanupContextDurationSink.OnStartCleanupContext","ITfCleanupContextDurationSink::OnStartCleanupContext","OnStartCleanupContext","OnStartCleanupContext method [Text Services Framework]","OnStartCleanupContext method [Text Services Framework]","ITfCleanupContextDurationSink interface","_tsf_itfcleanupcontextdurationsink_onstartcleanupcontext_ref","msctf/ITfCleanupContextDurationSink::OnStartCleanupContext","tsf.itfcleanupcontextdurationsink_onstartcleanupcontext"]
old-location: tsf\itfcleanupcontextdurationsink_onstartcleanupcontext.htm
tech.root: TSF
ms.assetid: a35aa7b1-273d-47ff-a705-298393f4abd2
ms.date: 12/05/2018
ms.keywords: ITfCleanupContextDurationSink interface [Text Services Framework],OnStartCleanupContext method, ITfCleanupContextDurationSink.OnStartCleanupContext, ITfCleanupContextDurationSink::OnStartCleanupContext, OnStartCleanupContext, OnStartCleanupContext method [Text Services Framework], OnStartCleanupContext method [Text Services Framework],ITfCleanupContextDurationSink interface, _tsf_itfcleanupcontextdurationsink_onstartcleanupcontext_ref, msctf/ITfCleanupContextDurationSink::OnStartCleanupContext, tsf.itfcleanupcontextdurationsink_onstartcleanupcontext
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
 - ITfCleanupContextDurationSink::OnStartCleanupContext
 - msctf/ITfCleanupContextDurationSink::OnStartCleanupContext
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
 - ITfCleanupContextDurationSink.OnStartCleanupContext
---

# ITfCleanupContextDurationSink::OnStartCleanupContext


## -description

Called when a context cleanup operation is about to begin.



## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

A context cleanup occurs when:

- The text service is deactivated while a context is still on the context stack. This can occur when the active text service is changed or when the active language changes while the text service is active.
- [ITfThreadMgr::Deactivate](nf-msctf-itfthreadmgr-deactivate.md) is called while a context is still on the context stack.

[ITfCleanupContextDurationSink::OnStartCleanupContext](nf-msctf-itfcleanupcontextdurationsink-onstartcleanupcontext.md) is called just before the TSF manager begins making [ITfCleanupContextSink::OnCleanupContext](nf-msctf-itfcleanupcontextsink-oncleanupcontext.md) notifications. When all of the OnCleanupContext notifications complete, the TSF manager calls **OnEndCleanupContext**.

## -see-also

[ITfCleanupContextDurationSink interface](nn-msctf-itfcleanupcontextdurationsink.md), [ITfCleanupContextDurationSink::OnEndCleanupContext](nf-msctf-itfcleanupcontextdurationsink-onendcleanupcontext.md), [ITfCleanupContextSink::OnCleanupContext](nf-msctf-itfcleanupcontextsink-oncleanupcontext.md)

