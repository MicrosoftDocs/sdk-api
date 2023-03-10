---
UID: NF:msctf.ITfThreadMgrEventSink.OnInitDocumentMgr
title: ITfThreadMgrEventSink::OnInitDocumentMgr (msctf.h)
description: ITfThreadMgrEventSink::OnInitDocumentMgr method
helpviewer_keywords: ["ITfThreadMgrEventSink interface [Text Services Framework]","OnInitDocumentMgr method","ITfThreadMgrEventSink.OnInitDocumentMgr","ITfThreadMgrEventSink::OnInitDocumentMgr","OnInitDocumentMgr","OnInitDocumentMgr method [Text Services Framework]","OnInitDocumentMgr method [Text Services Framework]","ITfThreadMgrEventSink interface","_tsf_itfthreadmgreventsink_oninitdocumentmgr_ref","msctf/ITfThreadMgrEventSink::OnInitDocumentMgr","tsf.itfthreadmgreventsink_oninitdocumentmgr"]
old-location: tsf\itfthreadmgreventsink_oninitdocumentmgr.htm
tech.root: TSF
ms.assetid: 18586e51-66b6-4071-88b4-9b92d5449a45
ms.date: 12/05/2018
ms.keywords: ITfThreadMgrEventSink interface [Text Services Framework],OnInitDocumentMgr method, ITfThreadMgrEventSink.OnInitDocumentMgr, ITfThreadMgrEventSink::OnInitDocumentMgr, OnInitDocumentMgr, OnInitDocumentMgr method [Text Services Framework], OnInitDocumentMgr method [Text Services Framework],ITfThreadMgrEventSink interface, _tsf_itfthreadmgreventsink_oninitdocumentmgr_ref, msctf/ITfThreadMgrEventSink::OnInitDocumentMgr, tsf.itfthreadmgreventsink_oninitdocumentmgr
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
 - ITfThreadMgrEventSink::OnInitDocumentMgr
 - msctf/ITfThreadMgrEventSink::OnInitDocumentMgr
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
 - ITfThreadMgrEventSink.OnInitDocumentMgr
---

# ITfThreadMgrEventSink::OnInitDocumentMgr


## -description

Called when the first context is added to the context stack

## -parameters

### -param pdim [in]

Pointer to the document manager object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-push">ITfDocumentMgr::Push
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgreventsink">ITfThreadMgrEventSink</a>