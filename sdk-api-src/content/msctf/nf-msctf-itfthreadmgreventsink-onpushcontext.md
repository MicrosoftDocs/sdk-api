---
UID: NF:msctf.ITfThreadMgrEventSink.OnPushContext
title: ITfThreadMgrEventSink::OnPushContext (msctf.h)
description: ITfThreadMgrEventSink::OnPushContext method
helpviewer_keywords: ["ITfThreadMgrEventSink interface [Text Services Framework]","OnPushContext method","ITfThreadMgrEventSink.OnPushContext","ITfThreadMgrEventSink::OnPushContext","OnPushContext","OnPushContext method [Text Services Framework]","OnPushContext method [Text Services Framework]","ITfThreadMgrEventSink interface","_tsf_itfthreadmgreventsink_onpushcontext_ref","msctf/ITfThreadMgrEventSink::OnPushContext","tsf.itfthreadmgreventsink_onpushcontext"]
old-location: tsf\itfthreadmgreventsink_onpushcontext.htm
tech.root: TSF
ms.assetid: 80fbb861-1a12-4a9a-8f96-332c2f736f2d
ms.date: 12/05/2018
ms.keywords: ITfThreadMgrEventSink interface [Text Services Framework],OnPushContext method, ITfThreadMgrEventSink.OnPushContext, ITfThreadMgrEventSink::OnPushContext, OnPushContext, OnPushContext method [Text Services Framework], OnPushContext method [Text Services Framework],ITfThreadMgrEventSink interface, _tsf_itfthreadmgreventsink_onpushcontext_ref, msctf/ITfThreadMgrEventSink::OnPushContext, tsf.itfthreadmgreventsink_onpushcontext
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfThreadMgrEventSink::OnPushContext
 - msctf/ITfThreadMgrEventSink::OnPushContext
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
 - ITfThreadMgrEventSink.OnPushContext
---

# ITfThreadMgrEventSink::OnPushContext


## -description

Called when a context is added to the context stack

## -parameters

### -param pic [in]

Pointer to the context added to the stack.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-push">ITfDocumentMgr::Push
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgreventsink">ITfThreadMgrEventSink</a>