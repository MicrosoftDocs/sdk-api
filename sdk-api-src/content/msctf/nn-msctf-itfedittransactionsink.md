---
UID: NN:msctf.ITfEditTransactionSink
title: ITfEditTransactionSink
author: windows-sdk-content
description: The ITfEditTransactionSink interface is implemented by a text service and used by the TSF manager to support edit transactions.
old-location: tsf\itfedittransactionsink.htm
old-project: TSF
ms.assetid: d5393459-8bd6-4daf-830a-aa08d76c6347
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: ITfEditTransactionSink, ITfEditTransactionSink interface [Text Services Framework], ITfEditTransactionSink interface [Text Services Framework],described, _tsf_itfedittransactionsink_ref, msctf/ITfEditTransactionSink, tsf.itfedittransactionsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
-	ITfEditTransactionSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Imekrcic.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfEditTransactionSink interface


## -description


The <b>ITfEditTransactionSink</b> interface is implemented by a text service and used by the TSF manager to support edit transactions. An edit transaction is a series of edits that use multiple document locks. A text service can optionally implement this interface. This advise sink is installed by calling <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with IID_ITfEditTransactionSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfEditTransactionSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfEditTransactionSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9ca9eac8-f30b-4a52-b851-3ad7a5c4dfb7">OnEndEditTransaction</a>
</td>
<td align="left" width="63%">
Indicates the end of an edit transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf10e7aa-c2a1-4d7f-828a-434c9852f4d6">OnStartEditTransaction</a>
</td>
<td align="left" width="63%">
Indicates the start of an edit transaction.

</td>
</tr>
</table> 


## -remarks



An edit transaction involves multiple document locks, and usually includes multiple <a href="https://msdn.microsoft.com/7763a879-a558-463d-837b-e38e6f84b9f7">ITfTextEditSink::OnEndEdit</a> method callbacks.




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">
        ITfSource::AdviseSink
      </a>



<a href="https://msdn.microsoft.com/7763a879-a558-463d-837b-e38e6f84b9f7">
        ITfTextEditSink::OnEndEdit
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

