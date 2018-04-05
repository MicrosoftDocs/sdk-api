---
UID: NF:textstor.ITextStoreACPSink.OnEndEditTransaction
title: ITextStoreACPSink::OnEndEditTransaction method
author: windows-driver-content
description: ITextStoreACPSink::OnEndEditTransaction method
old-location: tsf\itextstoreacpsink_onendedittransaction.htm
old-project: TSF
ms.assetid: 4d2819a2-c780-47bb-b3e5-0836b8b4c5dd
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITextStoreACPSink, ITextStoreACPSink interface [Text Services Framework], OnEndEditTransaction method, ITextStoreACPSink::OnEndEditTransaction, OnEndEditTransaction method [Text Services Framework], OnEndEditTransaction method [Text Services Framework], ITextStoreACPSink interface, OnEndEditTransaction,ITextStoreACPSink.OnEndEditTransaction, _tsf_itextstoreacpsink_onendedittransaction_ref, textstor/ITextStoreACPSink::OnEndEditTransaction, tsf.itextstoreacpsink_onendedittransaction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreACPSink.OnEndEditTransaction
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACPSink::OnEndEditTransaction method


## -description




## -parameters






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



This method causes the <a href="https://msdn.microsoft.com/9ca9eac8-f30b-4a52-b851-3ad7a5c4dfb7">ITfEditTransactionSink::OnEndEditTransaction</a> method to be called on all installed edit transaction sinks.

An edit transaction is a group of text changes that should be processed at one time. Calling <a href="https://msdn.microsoft.com/1d5452a1-b2f3-42d6-a32d-95965c2af8d3">ITextStoreACPSink::OnStartEditTransaction</a> allows a text service to queue the upcoming changes until <b>ITextStoreACPSink::OnEndEditTransaction</b> is called. When <b>ITextStoreACPSink::OnEndEditTransaction</b> is called, the text service will process all of the queued changes. Use of edit transactions is optional.




## -see-also




<a href="https://msdn.microsoft.com/d7e5a04f-7159-436e-a522-4cb63063aeef">ITextStoreACPSink</a>



<a href="https://msdn.microsoft.com/1d5452a1-b2f3-42d6-a32d-95965c2af8d3">
        ITextStoreACPSink::OnStartEditTransaction
      </a>



<a href="https://msdn.microsoft.com/9ca9eac8-f30b-4a52-b851-3ad7a5c4dfb7">ITfEditTransactionSink::OnEndEditTransaction
      </a>
 

 

