---
UID: NF:msctf.ITfEditTransactionSink.OnStartEditTransaction
title: ITfEditTransactionSink::OnStartEditTransaction (msctf.h)
description: ITfEditTransactionSink::OnStartEditTransaction method
helpviewer_keywords: ["ITfEditTransactionSink interface [Text Services Framework]","OnStartEditTransaction method","ITfEditTransactionSink.OnStartEditTransaction","ITfEditTransactionSink::OnStartEditTransaction","OnStartEditTransaction","OnStartEditTransaction method [Text Services Framework]","OnStartEditTransaction method [Text Services Framework]","ITfEditTransactionSink interface","_tsf_itfedittransactionsink_onstartedittransaction_ref","msctf/ITfEditTransactionSink::OnStartEditTransaction","tsf.itfedittransactionsink_onstartedittransaction"]
old-location: tsf\itfedittransactionsink_onstartedittransaction.htm
tech.root: TSF
ms.assetid: cf10e7aa-c2a1-4d7f-828a-434c9852f4d6
ms.date: 12/05/2018
ms.keywords: ITfEditTransactionSink interface [Text Services Framework],OnStartEditTransaction method, ITfEditTransactionSink.OnStartEditTransaction, ITfEditTransactionSink::OnStartEditTransaction, OnStartEditTransaction, OnStartEditTransaction method [Text Services Framework], OnStartEditTransaction method [Text Services Framework],ITfEditTransactionSink interface, _tsf_itfedittransactionsink_onstartedittransaction_ref, msctf/ITfEditTransactionSink::OnStartEditTransaction, tsf.itfedittransactionsink_onstartedittransaction
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
 - ITfEditTransactionSink::OnStartEditTransaction
 - msctf/ITfEditTransactionSink::OnStartEditTransaction
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
 - ITfEditTransactionSink.OnStartEditTransaction
---

# ITfEditTransactionSink::OnStartEditTransaction


## -description

Indicates the start of an edit transaction.

## -parameters

### -param pic [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> interface involved in the transaction.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The TSF manager calls this method at the start of an edit transaction. A text service might delay reevaluation of the changing context of the transaction due to the multiple <a href="/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit</a> notifications until after receiving the corresponding <a href="/windows/desktop/api/msctf/nf-msctf-itfedittransactionsink-onendedittransaction">ITfEditTransactionSink::OnEndEditTransaction</a> callback.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfedittransactionsink">ITfEditTransactionSink
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfedittransactionsink-onendedittransaction">ITfEditTransactionSink::OnEndEditTransaction
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit
      </a>