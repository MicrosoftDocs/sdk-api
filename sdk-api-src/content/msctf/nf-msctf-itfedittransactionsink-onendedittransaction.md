---
UID: NF:msctf.ITfEditTransactionSink.OnEndEditTransaction
title: ITfEditTransactionSink::OnEndEditTransaction (msctf.h)
description: ITfEditTransactionSink::OnEndEditTransaction method
helpviewer_keywords: ["ITfEditTransactionSink interface [Text Services Framework]","OnEndEditTransaction method","ITfEditTransactionSink.OnEndEditTransaction","ITfEditTransactionSink::OnEndEditTransaction","OnEndEditTransaction","OnEndEditTransaction method [Text Services Framework]","OnEndEditTransaction method [Text Services Framework]","ITfEditTransactionSink interface","_tsf_itfedittransactionsink_onendedittransaction_ref","msctf/ITfEditTransactionSink::OnEndEditTransaction","tsf.itfedittransactionsink_onendedittransaction"]
old-location: tsf\itfedittransactionsink_onendedittransaction.htm
tech.root: TSF
ms.assetid: 9ca9eac8-f30b-4a52-b851-3ad7a5c4dfb7
ms.date: 12/05/2018
ms.keywords: ITfEditTransactionSink interface [Text Services Framework],OnEndEditTransaction method, ITfEditTransactionSink.OnEndEditTransaction, ITfEditTransactionSink::OnEndEditTransaction, OnEndEditTransaction, OnEndEditTransaction method [Text Services Framework], OnEndEditTransaction method [Text Services Framework],ITfEditTransactionSink interface, _tsf_itfedittransactionsink_onendedittransaction_ref, msctf/ITfEditTransactionSink::OnEndEditTransaction, tsf.itfedittransactionsink_onendedittransaction
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
 - ITfEditTransactionSink::OnEndEditTransaction
 - msctf/ITfEditTransactionSink::OnEndEditTransaction
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
 - ITfEditTransactionSink.OnEndEditTransaction
---

# ITfEditTransactionSink::OnEndEditTransaction


## -description

Indicates the end of an edit transaction.

## -parameters

### -param pic [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> interface involved in the transaction.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The TSF manager calls this method at the end of an edit transaction. A text service can delay reevaluation of the changing context of the transaction due to the multiple <a href="/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit</a> method notifications until after receiving this callback.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfedittransactionsink">ITfEditTransactionSink
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit
      </a>