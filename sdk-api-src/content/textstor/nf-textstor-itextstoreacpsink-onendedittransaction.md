---
UID: NF:textstor.ITextStoreACPSink.OnEndEditTransaction
title: ITextStoreACPSink::OnEndEditTransaction (textstor.h)
description: ITextStoreACPSink::OnEndEditTransaction method
helpviewer_keywords: ["ITextStoreACPSink interface [Text Services Framework]","OnEndEditTransaction method","ITextStoreACPSink.OnEndEditTransaction","ITextStoreACPSink::OnEndEditTransaction","OnEndEditTransaction","OnEndEditTransaction method [Text Services Framework]","OnEndEditTransaction method [Text Services Framework]","ITextStoreACPSink interface","_tsf_itextstoreacpsink_onendedittransaction_ref","textstor/ITextStoreACPSink::OnEndEditTransaction","tsf.itextstoreacpsink_onendedittransaction"]
old-location: tsf\itextstoreacpsink_onendedittransaction.htm
tech.root: TSF
ms.assetid: 4d2819a2-c780-47bb-b3e5-0836b8b4c5dd
ms.date: 12/05/2018
ms.keywords: ITextStoreACPSink interface [Text Services Framework],OnEndEditTransaction method, ITextStoreACPSink.OnEndEditTransaction, ITextStoreACPSink::OnEndEditTransaction, OnEndEditTransaction, OnEndEditTransaction method [Text Services Framework], OnEndEditTransaction method [Text Services Framework],ITextStoreACPSink interface, _tsf_itextstoreacpsink_onendedittransaction_ref, textstor/ITextStoreACPSink::OnEndEditTransaction, tsf.itextstoreacpsink_onendedittransaction
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
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
 - ITextStoreACPSink::OnEndEditTransaction
 - textstor/ITextStoreACPSink::OnEndEditTransaction
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
 - ITextStoreACPSink.OnEndEditTransaction
---

# ITextStoreACPSink::OnEndEditTransaction


## -description

Called when an edit transaction is terminated.



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
</table>

## -remarks

This method causes the <a href="/windows/desktop/api/msctf/nf-msctf-itfedittransactionsink-onendedittransaction">ITfEditTransactionSink::OnEndEditTransaction</a> method to be called on all installed edit transaction sinks.

An edit transaction is a group of text changes that should be processed at one time. Calling <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onstartedittransaction">ITextStoreACPSink::OnStartEditTransaction</a> allows a text service to queue the upcoming changes until <b>ITextStoreACPSink::OnEndEditTransaction</b> is called. When <b>ITextStoreACPSink::OnEndEditTransaction</b> is called, the text service will process all of the queued changes. Use of edit transactions is optional.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacpsink">ITextStoreACPSink</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onstartedittransaction">ITextStoreACPSink::OnStartEditTransaction
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfedittransactionsink-onendedittransaction">ITfEditTransactionSink::OnEndEditTransaction
      </a>
