---
UID: NF:msctf.ITfThreadMgrEventSink.OnUninitDocumentMgr
title: ITfThreadMgrEventSink::OnUninitDocumentMgr (msctf.h)
description: ITfThreadMgrEventSink::OnUninitDocumentMgr method
helpviewer_keywords: ["ITfThreadMgrEventSink interface [Text Services Framework]","OnUninitDocumentMgr method","ITfThreadMgrEventSink.OnUninitDocumentMgr","ITfThreadMgrEventSink::OnUninitDocumentMgr","OnUninitDocumentMgr","OnUninitDocumentMgr method [Text Services Framework]","OnUninitDocumentMgr method [Text Services Framework]","ITfThreadMgrEventSink interface","_tsf_itfthreadmgreventsink_onuninitdocumentmgr_ref","msctf/ITfThreadMgrEventSink::OnUninitDocumentMgr","tsf.itfthreadmgreventsink_onuninitdocumentmgr"]
old-location: tsf\itfthreadmgreventsink_onuninitdocumentmgr.htm
tech.root: TSF
ms.assetid: da4532e4-aa00-41af-8dfc-1880dc5b3b22
ms.date: 12/05/2018
ms.keywords: ITfThreadMgrEventSink interface [Text Services Framework],OnUninitDocumentMgr method, ITfThreadMgrEventSink.OnUninitDocumentMgr, ITfThreadMgrEventSink::OnUninitDocumentMgr, OnUninitDocumentMgr, OnUninitDocumentMgr method [Text Services Framework], OnUninitDocumentMgr method [Text Services Framework],ITfThreadMgrEventSink interface, _tsf_itfthreadmgreventsink_onuninitdocumentmgr_ref, msctf/ITfThreadMgrEventSink::OnUninitDocumentMgr, tsf.itfthreadmgreventsink_onuninitdocumentmgr
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
 - ITfThreadMgrEventSink::OnUninitDocumentMgr
 - msctf/ITfThreadMgrEventSink::OnUninitDocumentMgr
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
 - ITfThreadMgrEventSink.OnUninitDocumentMgr
---

# ITfThreadMgrEventSink::OnUninitDocumentMgr


## -description

Called when the last context is removed from the context stack

## -parameters

### -param pdim [in]

Pointer to the document manager object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-pop">ITfDocumentMgr::Pop
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgreventsink">ITfThreadMgrEventSink</a>