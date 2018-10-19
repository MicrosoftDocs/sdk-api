---
UID: NF:textstor.ITextStoreACPSink.OnStartEditTransaction
title: ITextStoreACPSink::OnStartEditTransaction
author: windows-sdk-content
description: ITextStoreACPSink::OnStartEditTransaction method
old-location: tsf\itextstoreacpsink_onstartedittransaction.htm
tech.root: TSF
ms.assetid: 1d5452a1-b2f3-42d6-a32d-95965c2af8d3
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITextStoreACPSink interface [Text Services Framework],OnStartEditTransaction method, ITextStoreACPSink.OnStartEditTransaction, ITextStoreACPSink::OnStartEditTransaction, OnStartEditTransaction, OnStartEditTransaction method [Text Services Framework], OnStartEditTransaction method [Text Services Framework],ITextStoreACPSink interface, _tsf_itextstoreacpsink_onstartedittransaction_ref, textstor/ITextStoreACPSink::OnStartEditTransaction, tsf.itextstoreacpsink_onstartedittransaction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACPSink.OnStartEditTransaction
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreACPSink::OnStartEditTransaction


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



This method causes the <a href="https://msdn.microsoft.com/cf10e7aa-c2a1-4d7f-828a-434c9852f4d6">ITfEditTransactionSink::OnStartEditTransaction</a> method to be called on all installed edit transaction sinks.

An edit transaction is a group of text changes that should be processed at one time. Calling this method allows a text service to queue the upcoming changes until <a href="https://msdn.microsoft.com/4d2819a2-c780-47bb-b3e5-0836b8b4c5dd">ITextStoreACPSink::OnEndEditTransaction</a> is called. When <b>ITextStoreACPSink::OnEndEditTransaction</b> is called, the text service will process all queued changes. Use of edit transactions is optional.




## -see-also




<a href="https://msdn.microsoft.com/d7e5a04f-7159-436e-a522-4cb63063aeef">ITextStoreACPSink</a>



<a href="https://msdn.microsoft.com/4d2819a2-c780-47bb-b3e5-0836b8b4c5dd">ITextStoreACPSink::OnEndEditTransaction
      </a>



<a href="https://msdn.microsoft.com/cf10e7aa-c2a1-4d7f-828a-434c9852f4d6">ITfEditTransactionSink::OnStartEditTransaction
      </a>
 

 

