---
UID: NF:msctf.ITfTextEditSink.OnEndEdit
title: ITfTextEditSink::OnEndEdit (msctf.h)
description: ITfTextEditSink::OnEndEdit method
helpviewer_keywords: ["ITfTextEditSink interface [Text Services Framework]","OnEndEdit method","ITfTextEditSink.OnEndEdit","ITfTextEditSink::OnEndEdit","OnEndEdit","OnEndEdit method [Text Services Framework]","OnEndEdit method [Text Services Framework]","ITfTextEditSink interface","_tsf_itftexteditsink_onendedit_ref","msctf/ITfTextEditSink::OnEndEdit","tsf.itftexteditsink_onendedit"]
old-location: tsf\itftexteditsink_onendedit.htm
tech.root: TSF
ms.assetid: 7763a879-a558-463d-837b-e38e6f84b9f7
ms.date: 12/05/2018
ms.keywords: ITfTextEditSink interface [Text Services Framework],OnEndEdit method, ITfTextEditSink.OnEndEdit, ITfTextEditSink::OnEndEdit, OnEndEdit, OnEndEdit method [Text Services Framework], OnEndEdit method [Text Services Framework],ITfTextEditSink interface, _tsf_itftexteditsink_onendedit_ref, msctf/ITfTextEditSink::OnEndEdit, tsf.itftexteditsink_onendedit
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITfTextEditSink::OnEndEdit
 - msctf/ITfTextEditSink::OnEndEdit
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
 - ITfTextEditSink.OnEndEdit
---

# ITfTextEditSink::OnEndEdit


## -description

Receives a notification upon completion of an ITfEditSession::DoEditSession method that has read/write access to the context.

## -parameters

### -param pic [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> interface for the edited context.

### -param ecReadOnly [in]

Specifies a <a href="/windows/desktop/TSF/tfeditcookie">TfEditCookie</a> value for read-only access to the context.

### -param pEditRecord [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfeditrecord">ITfEditRecord</a> interface used to access the modifications to the context.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An edit session with read/write access is requested with a call to the <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-requesteditsession">ITfContext::RequestEditSession</a> method using the TF_ES_READWRITE flag, which establishes an <b>ITfEditSession::DoEditSession</b> method to perform the session. When such a <b>ITfEditSession::DoEditSession</b> method completes, TSF calls this method.

A text service can use the <i>ecReadOnly</i> parameter only to view the context. If changes are required, the text service must use an asynchronous call to the <b>ITfContext::RequestEditSession</b> method. However, a text service should modify only text that it previously entered as part of a composition. Otherwise, two or more text services could repeatedly modify the same text. A text service can use the <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-inwritesession">ITfContext::InWriteSession</a> method to determine if it performed the completed edit session.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-inwritesession">ITfContext::InWriteSession
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-requesteditsession">ITfContext::RequestEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfeditrecord">ITfEditRecord
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itftexteditsink">ITfTextEditSink</a>



<a href="/windows/desktop/TSF/tfeditcookie">TfEditCookie
      </a>