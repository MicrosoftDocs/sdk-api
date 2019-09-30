---
UID: NN:msctf.ITfEditTransactionSink
title: ITfEditTransactionSink (msctf.h)
author: windows-sdk-content
description: The ITfEditTransactionSink interface is implemented by a text service and used by the TSF manager to support edit transactions.
old-location: tsf\itfedittransactionsink.htm
tech.root: TSF
ms.assetid: d5393459-8bd6-4daf-830a-aa08d76c6347
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfEditTransactionSink, ITfEditTransactionSink interface [Text Services Framework], ITfEditTransactionSink interface [Text Services Framework],described, _tsf_itfedittransactionsink_ref, msctf/ITfEditTransactionSink, tsf.itfedittransactionsink
ms.topic: interface
f1_keywords: 
 - "msctf/ITfEditTransactionSink"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfEditTransactionSink
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfEditTransactionSink interface


## -description


The <b>ITfEditTransactionSink</b> interface is implemented by a text service and used by the TSF manager to support edit transactions. An edit transaction is a series of edits that use multiple document locks. A text service can optionally implement this interface. This advise sink is installed by calling <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfEditTransactionSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfEditTransactionSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfEditTransactionSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfEditTransactionSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfedittransactionsink-onendedittransaction">OnEndEditTransaction</a>
</td>
<td align="left" width="63%">
Indicates the end of an edit transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfedittransactionsink-onstartedittransaction">OnStartEditTransaction</a>
</td>
<td align="left" width="63%">
Indicates the start of an edit transaction.

</td>
</tr>
</table> 


## -remarks



An edit transaction involves multiple document locks, and usually includes multiple <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit</a> method callbacks.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftexteditsink-onendedit">ITfTextEditSink::OnEndEdit
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

