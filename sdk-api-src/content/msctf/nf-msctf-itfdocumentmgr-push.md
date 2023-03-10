---
UID: NF:msctf.ITfDocumentMgr.Push
title: ITfDocumentMgr::Push (msctf.h)
description: ITfDocumentMgr::Push method
helpviewer_keywords: ["ITfDocumentMgr interface [Text Services Framework]","Push method","ITfDocumentMgr.Push","ITfDocumentMgr::Push","Push","Push method [Text Services Framework]","Push method [Text Services Framework]","ITfDocumentMgr interface","_tsf_itfdocumentmgr_push_ref","msctf/ITfDocumentMgr::Push","tsf.itfdocumentmgr_push"]
old-location: tsf\itfdocumentmgr_push.htm
tech.root: TSF
ms.assetid: afd5452b-4121-428d-801f-1638c2767c67
ms.date: 12/05/2018
ms.keywords: ITfDocumentMgr interface [Text Services Framework],Push method, ITfDocumentMgr.Push, ITfDocumentMgr::Push, Push, Push method [Text Services Framework], Push method [Text Services Framework],ITfDocumentMgr interface, _tsf_itfdocumentmgr_push_ref, msctf/ITfDocumentMgr::Push, tsf.itfdocumentmgr_push
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfDocumentMgr::Push
 - msctf/ITfDocumentMgr::Push
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfDocumentMgr.Push
---

# ITfDocumentMgr::Push


## -description

Adds a context to the top of the context stack.

## -parameters

### -param pic [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> object to be added to the stack. This object is obtained from a previous call to <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pic</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_STACKFULL</b></dt>
</dl>
</td>
<td width="60%">
No space exists on the stack for the context. The context stack has a limit of two contexts.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This method was called during an <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-pop">ITfDocumentMgr::Pop</a> call.

</td>
</tr>
</table>

## -remarks

The first context added to the stack becomes the main document context.

The TSF manager and text services only interact with the context at the top of the stack. Normally, only the main document context is on the stack. Occasionally, it is necessary to add a second context to the stack. For example, when a text service must display a modal UI, such as a candidate list. During this time, the text service will add its context to the stack. When the text service UI is no longer required, the text service removes the context from the stack. The main context then returns to the top of the stack. To simplify this process and prevent multiple modal UIs from being displayed, there is a maximum of two contexts allowed on the stack.

This method causes the <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-onpushcontext">ITfThreadMgrEventSink::OnPushContext</a> method of all installed thread manager event sinks to be called. If this is the first context to be added to the stack, this method causes the <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-oninitdocumentmgr">ITfThreadMgrEventSink::OnInitDocumentMgr</a> method of all installed thread manager event sinks to be called.


<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-pop">ITfDocumentMgr::Pop</a> must be called to remove this context from the context stack.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-pop">ITfDocumentMgr::Pop
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-oninitdocumentmgr">ITfThreadMgrEventSink::OnInitDocumentMgr
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-onpushcontext">ITfThreadMgrEventSink::OnPushContext
      </a>