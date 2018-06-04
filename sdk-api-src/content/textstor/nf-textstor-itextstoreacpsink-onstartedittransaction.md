---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



<a href="https://msdn.microsoft.com/4d2819a2-c780-47bb-b3e5-0836b8b4c5dd">
        ITextStoreACPSink::OnEndEditTransaction
      </a>



<a href="https://msdn.microsoft.com/cf10e7aa-c2a1-4d7f-828a-434c9852f4d6">ITfEditTransactionSink::OnStartEditTransaction
      </a>
 

 

