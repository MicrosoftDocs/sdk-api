---
UID: NF:textstor.ITextStoreAnchorSink.OnStartEditTransaction
title: ITextStoreAnchorSink::OnStartEditTransaction
author: windows-driver-content
description: ITextStoreAnchorSink::OnStartEditTransaction method
old-location: tsf\itextstoreanchorsink_onstartedittransaction.htm
old-project: TSF
ms.assetid: 9e86d767-8ace-4bd0-af12-2139814b4e44
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITextStoreAnchorSink interface [Text Services Framework],OnStartEditTransaction method, ITextStoreAnchorSink.OnStartEditTransaction, ITextStoreAnchorSink::OnStartEditTransaction, OnStartEditTransaction, OnStartEditTransaction method [Text Services Framework], OnStartEditTransaction method [Text Services Framework],ITextStoreAnchorSink interface, _tsf_itextstoreanchorsink_onstartedittransaction_ref, textstor/ITextStoreAnchorSink::OnStartEditTransaction, tsf.itextstoreanchorsink_onstartedittransaction
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
-	ITextStoreAnchorSink.OnStartEditTransaction
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreAnchorSink::OnStartEditTransaction


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



This method will be called on all installed edit transaction sinks.

An edit transaction is a group of text changes that should be processed at one time. Calling this method allows a text service to queue the upcoming changes until <a href="https://msdn.microsoft.com/fe7610b3-02f0-491a-8c55-f9dc9843073b">ITextStoreAnchorSink::OnEndEditTransaction</a> is called. When <b>ITextStoreAnchorSink::OnEndEditTransaction</b> is called, the text service will process all queued changes.

Use of edit transactions is optional.




## -see-also




<a href="https://msdn.microsoft.com/fb96b4fb-864f-4f32-bf7c-cf7f199e552a">ITextStoreAnchorSink</a>



<a href="https://msdn.microsoft.com/fe7610b3-02f0-491a-8c55-f9dc9843073b">
        ITextStoreAnchorSink::OnEndEditTransaction
      </a>



<a href="https://msdn.microsoft.com/cf10e7aa-c2a1-4d7f-828a-434c9852f4d6">ITfEditTransactionSink::OnStartEditTransaction
      </a>
 

 

