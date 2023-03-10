---
UID: NN:msctf.ITfEditTransactionSink
title: ITfEditTransactionSink (msctf.h)
description: The ITfEditTransactionSink interface is implemented by a text service and used by the TSF manager to support edit transactions.
helpviewer_keywords: ["ITfEditTransactionSink","ITfEditTransactionSink interface [Text Services Framework]","ITfEditTransactionSink interface [Text Services Framework]","described","_tsf_itfedittransactionsink_ref","msctf/ITfEditTransactionSink","tsf.itfedittransactionsink"]
old-location: tsf\itfedittransactionsink.htm
tech.root: TSF
ms.assetid: d5393459-8bd6-4daf-830a-aa08d76c6347
ms.date: 12/05/2018
ms.keywords: ITfEditTransactionSink, ITfEditTransactionSink interface [Text Services Framework], ITfEditTransactionSink interface [Text Services Framework],described, _tsf_itfedittransactionsink_ref, msctf/ITfEditTransactionSink, tsf.itfedittransactionsink
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
 - ITfEditTransactionSink
 - msctf/ITfEditTransactionSink
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
 - ITfEditTransactionSink
---

# ITfEditTransactionSink interface


## -description

The <b>ITfEditTransactionSink</b> interface is implemented by a text service and used by the TSF manager to support edit transactions. An edit transaction is a series of edits that use multiple document locks. A text service can optionally implement this interface. This advise sink is installed by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfEditTransactionSink.

## -inheritance

The <b>ITfEditTransactionSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfEditTransactionSink</b> also has these types of members:

## -remarks

An edit transaction involves multiple document locks, and usually includes multiple <a href="/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit</a> method callbacks.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
