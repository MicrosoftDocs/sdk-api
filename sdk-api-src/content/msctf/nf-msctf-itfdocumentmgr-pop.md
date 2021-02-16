---
UID: NF:msctf.ITfDocumentMgr.Pop
title: ITfDocumentMgr::Pop (msctf.h)
description: ITfDocumentMgr::Pop method
helpviewer_keywords: ["ITfDocumentMgr interface [Text Services Framework]","Pop method","ITfDocumentMgr.Pop","ITfDocumentMgr::Pop","Pop","Pop method [Text Services Framework]","Pop method [Text Services Framework]","ITfDocumentMgr interface","_tsf_itfdocumentmgr_pop_ref","msctf/ITfDocumentMgr::Pop","tsf.itfdocumentmgr_pop"]
old-location: tsf\itfdocumentmgr_pop.htm
tech.root: TSF
ms.assetid: bbf65d8d-5a59-4c4b-a132-fa28babcd70b
ms.date: 12/05/2018
ms.keywords: ITfDocumentMgr interface [Text Services Framework],Pop method, ITfDocumentMgr.Pop, ITfDocumentMgr::Pop, Pop, Pop method [Text Services Framework], Pop method [Text Services Framework],ITfDocumentMgr interface, _tsf_itfdocumentmgr_pop_ref, msctf/ITfDocumentMgr::Pop, tsf.itfdocumentmgr_pop
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
 - ITfDocumentMgr::Pop
 - msctf/ITfDocumentMgr::Pop
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
 - ITfDocumentMgr.Pop
---

# ITfDocumentMgr::Pop


## -description

Removes the context from the top of the context stack.

## -parameters

### -param dwFlags [in]

If this value is 0, only the context at the top of the stack is removed. If this value is TF_POPF_ALL, all of the contexts are removed from the stack.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The stack is empty or this method is called without the TF_POPF_ALL flag and only a single context is on the stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This method was called during another <b>ITfDocumentMgr::Pop</b> call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwFlags</i> is invalid.

</td>
</tr>
</table>

## -remarks

This method must be called from the same thread as the corresponding <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-push">ITfDocumentMgr::Push</a> call.

The first context added to the stack becomes the primary context. The primary context cannot be removed from the stack without using the TF_POPF_ALL flag. When the document is uninitialized, this method should be called with the TF_POPF_ALL flag. This causes the document manager to remove all contexts from the context stack and terminate any text service UI. Do not use the TF_POPF_ALL flag at any other time.

This method causes the <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-onpopcontext">ITfThreadMgrEventSink::OnPopContext</a> method of all installed thread manager event sinks to be called. If the last context is removed from the stack, this method causes the <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-onuninitdocumentmgr">ITfThreadMgrEventSink::OnUninitDocumentMgr</a> method of all installed thread manager event sinks to be called.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-push">ITfDocumentMgr::Push
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-onpopcontext">ITfThreadMgrEventSink::OnPopContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgreventsink-onuninitdocumentmgr">ITfThreadMgrEventSink::OnUninitDocumentMgr
      </a>