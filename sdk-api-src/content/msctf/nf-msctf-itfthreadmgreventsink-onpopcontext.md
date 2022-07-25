---
UID: NF:msctf.ITfThreadMgrEventSink.OnPopContext
title: ITfThreadMgrEventSink::OnPopContext (msctf.h)
description: ITfThreadMgrEventSink::OnPopContext method
helpviewer_keywords: ["ITfThreadMgrEventSink interface [Text Services Framework]","OnPopContext method","ITfThreadMgrEventSink.OnPopContext","ITfThreadMgrEventSink::OnPopContext","OnPopContext","OnPopContext method [Text Services Framework]","OnPopContext method [Text Services Framework]","ITfThreadMgrEventSink interface","_tsf_itfthreadmgreventsink_onpopcontext_ref","msctf/ITfThreadMgrEventSink::OnPopContext","tsf.itfthreadmgreventsink_onpopcontext"]
old-location: tsf\itfthreadmgreventsink_onpopcontext.htm
tech.root: TSF
ms.assetid: de07d7cf-db91-44e0-a0b2-4de26262552f
ms.date: 12/05/2018
ms.keywords: ITfThreadMgrEventSink interface [Text Services Framework],OnPopContext method, ITfThreadMgrEventSink.OnPopContext, ITfThreadMgrEventSink::OnPopContext, OnPopContext, OnPopContext method [Text Services Framework], OnPopContext method [Text Services Framework],ITfThreadMgrEventSink interface, _tsf_itfthreadmgreventsink_onpopcontext_ref, msctf/ITfThreadMgrEventSink::OnPopContext, tsf.itfthreadmgreventsink_onpopcontext
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfThreadMgrEventSink::OnPopContext
 - msctf/ITfThreadMgrEventSink::OnPopContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfThreadMgrEventSink.OnPopContext
---

# ITfThreadMgrEventSink::OnPopContext


## -description

Called when a context is removed from the context stack

## -parameters

### -param pic [in]

Pointer to the context removed from the stack.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-pop">ITfDocumentMgr::Pop
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgreventsink">ITfThreadMgrEventSink</a>