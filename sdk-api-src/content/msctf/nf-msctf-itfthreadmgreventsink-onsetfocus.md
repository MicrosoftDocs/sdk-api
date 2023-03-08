---
UID: NF:msctf.ITfThreadMgrEventSink.OnSetFocus
title: ITfThreadMgrEventSink::OnSetFocus (msctf.h)
description: ITfThreadMgrEventSink::OnSetFocus method
helpviewer_keywords: ["ITfThreadMgrEventSink interface [Text Services Framework]","OnSetFocus method","ITfThreadMgrEventSink.OnSetFocus","ITfThreadMgrEventSink::OnSetFocus","OnSetFocus","OnSetFocus method [Text Services Framework]","OnSetFocus method [Text Services Framework]","ITfThreadMgrEventSink interface","_tsf_itfthreadmgreventsink_onsetfocus_ref","msctf/ITfThreadMgrEventSink::OnSetFocus","tsf.itfthreadmgreventsink_onsetfocus"]
old-location: tsf\itfthreadmgreventsink_onsetfocus.htm
tech.root: TSF
ms.assetid: 2c8f2b0a-5b56-4814-bed4-6875a09de176
ms.date: 12/05/2018
ms.keywords: ITfThreadMgrEventSink interface [Text Services Framework],OnSetFocus method, ITfThreadMgrEventSink.OnSetFocus, ITfThreadMgrEventSink::OnSetFocus, OnSetFocus, OnSetFocus method [Text Services Framework], OnSetFocus method [Text Services Framework],ITfThreadMgrEventSink interface, _tsf_itfthreadmgreventsink_onsetfocus_ref, msctf/ITfThreadMgrEventSink::OnSetFocus, tsf.itfthreadmgreventsink_onsetfocus
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
 - ITfThreadMgrEventSink::OnSetFocus
 - msctf/ITfThreadMgrEventSink::OnSetFocus
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
 - ITfThreadMgrEventSink.OnSetFocus
---

# ITfThreadMgrEventSink::OnSetFocus


## -description

Called when a document view receives or loses the focus

## -parameters

### -param pdimFocus [in]

Pointer to the document manager receiving the input focus. If no document is receiving the focus, this will be <b>NULL</b>.

### -param pdimPrevFocus [in]

Pointer to the document manager that previously had the input focus. If no document had the focus, this will be <b>NULL</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-setfocus">ITfThreadMgr::SetFocus
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgreventsink">ITfThreadMgrEventSink</a>