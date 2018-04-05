---
UID: NF:msctf.ITfEditTransactionSink.OnEndEditTransaction
title: ITfEditTransactionSink::OnEndEditTransaction method
author: windows-driver-content
description: ITfEditTransactionSink::OnEndEditTransaction method
old-location: tsf\itfedittransactionsink_onendedittransaction.htm
old-project: TSF
ms.assetid: 9ca9eac8-f30b-4a52-b851-3ad7a5c4dfb7
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfEditTransactionSink, ITfEditTransactionSink interface [Text Services Framework], OnEndEditTransaction method, ITfEditTransactionSink::OnEndEditTransaction, OnEndEditTransaction method [Text Services Framework], OnEndEditTransaction method [Text Services Framework], ITfEditTransactionSink interface, OnEndEditTransaction,ITfEditTransactionSink.OnEndEditTransaction, _tsf_itfedittransactionsink_onendedittransaction_ref, msctf/ITfEditTransactionSink::OnEndEditTransaction, tsf.itfedittransactionsink_onendedittransaction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imekrcic.dll
api_name:
-	ITfEditTransactionSink.OnEndEditTransaction
product: Windows
targetos: Windows
req.lib: 
req.dll: Imekrcic.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfEditTransactionSink::OnEndEditTransaction method


## -description




## -parameters




### -param pic [in]

Pointer to the <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> interface involved in the transaction.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The TSF manager calls this method at the end of an edit transaction. A text service can delay reevaluation of the changing context of the transaction due to the multiple <a href="https://msdn.microsoft.com/7763a879-a558-463d-837b-e38e6f84b9f7">ITfTextEditSink::OnEndEdit</a> method notifications until after receiving this callback.




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/d5393459-8bd6-4daf-830a-aa08d76c6347">
        ITfEditTransactionSink
      </a>



<a href="https://msdn.microsoft.com/7763a879-a558-463d-837b-e38e6f84b9f7">
        ITfTextEditSink::OnEndEdit
      </a>
 

 

