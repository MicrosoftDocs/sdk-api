---
UID: NF:msctf.ITfCleanupContextSink.OnCleanupContext
title: ITfCleanupContextSink::OnCleanupContext (msctf.h)
description: ITfCleanupContextSink::OnCleanupContext method
helpviewer_keywords: ["ITfCleanupContextSink interface [Text Services Framework]","OnCleanupContext method","ITfCleanupContextSink.OnCleanupContext","ITfCleanupContextSink::OnCleanupContext","OnCleanupContext","OnCleanupContext method [Text Services Framework]","OnCleanupContext method [Text Services Framework]","ITfCleanupContextSink interface","_tsf_itfcleanupcontextsink_oncleanupcontext_ref","msctf/ITfCleanupContextSink::OnCleanupContext","tsf.itfcleanupcontextsink_oncleanupcontext"]
old-location: tsf\itfcleanupcontextsink_oncleanupcontext.htm
tech.root: TSF
ms.assetid: 6af597e6-f997-4b28-8994-a8dbabcaaa68
ms.date: 12/05/2018
ms.keywords: ITfCleanupContextSink interface [Text Services Framework],OnCleanupContext method, ITfCleanupContextSink.OnCleanupContext, ITfCleanupContextSink::OnCleanupContext, OnCleanupContext, OnCleanupContext method [Text Services Framework], OnCleanupContext method [Text Services Framework],ITfCleanupContextSink interface, _tsf_itfcleanupcontextsink_oncleanupcontext_ref, msctf/ITfCleanupContextSink::OnCleanupContext, tsf.itfcleanupcontextsink_oncleanupcontext
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
 - ITfCleanupContextSink::OnCleanupContext
 - msctf/ITfCleanupContextSink::OnCleanupContext
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
 - ITfCleanupContextSink.OnCleanupContext
---

# ITfCleanupContextSink::OnCleanupContext


## -description

Called during a context cleanup operation.

## -parameters

### -param ecWrite [in]

Contains a <a href="/windows/desktop/TSF/tfeditcookie">TfEditCookie</a> value that identifies the edit context cleaned up. The edit context is guaranteed to have a read/write lock.

### -param pic [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> interface that represents the context cleaned up.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

A context cleanup occurs when:

- The text service is deactivated while a context is still on the context stack. This can occur when the active text service is changed or when the active language changes while the text service is active.
- [ITfThreadMgr::Deactivate](nf-msctf-itfthreadmgr-deactivate.md) is called while a context is still on the context stack.

[ITfCleanupContextDurationSink::OnStartCleanupContext](nf-msctf-itfcleanupcontextdurationsink-onstartcleanupcontext.md) is called just before the TSF manager begins making [ITfCleanupContextSink::OnCleanupContext](nf-msctf-itfcleanupcontextsink-oncleanupcontext.md) notifications. When all of the OnCleanupContext notifications complete, the TSF manager calls **OnEndCleanupContext**.

## -see-also

[ITfCleanupContextSink interface](nn-msctf-itfcleanupcontextsink.md), [ITfContext interface](nn-msctf-itfcontext.md), [TfEditCookie](/windows/win32/tsf/tfeditcookie)