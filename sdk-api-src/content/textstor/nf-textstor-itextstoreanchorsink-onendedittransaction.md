---
UID: NF:textstor.ITextStoreAnchorSink.OnEndEditTransaction
title: ITextStoreAnchorSink::OnEndEditTransaction
author: windows-sdk-content
description: ITextStoreAnchorSink::OnEndEditTransaction method
old-location: tsf\itextstoreanchorsink_onendedittransaction.htm
old-project: TSF
ms.assetid: fe7610b3-02f0-491a-8c55-f9dc9843073b
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITextStoreAnchorSink interface [Text Services Framework],OnEndEditTransaction method, ITextStoreAnchorSink.OnEndEditTransaction, ITextStoreAnchorSink::OnEndEditTransaction, OnEndEditTransaction, OnEndEditTransaction method [Text Services Framework], OnEndEditTransaction method [Text Services Framework],ITextStoreAnchorSink interface, _tsf_itextstoreanchorsink_onendedittransaction_ref, textstor/ITextStoreAnchorSink::OnEndEditTransaction, tsf.itextstoreanchorsink_onendedittransaction
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreAnchorSink.OnEndEditTransaction
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreAnchorSink::OnEndEditTransaction


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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The reference count of the edit transaction is incorrect.

</td>
</tr>
</table>
 




## -remarks



This method causes the <a href="https://msdn.microsoft.com/9ca9eac8-f30b-4a52-b851-3ad7a5c4dfb7">ITfEditTransactionSink::OnEndEditTransaction</a> method to be called on all installed edit transaction sinks.

An edit transaction is a group of text changes that should be processed at one time. Calling <a href="https://msdn.microsoft.com/9e86d767-8ace-4bd0-af12-2139814b4e44">ITextStoreAnchorSink::OnStartEditTransaction</a> allows a text service to queue the upcoming changes until <b>ITextStoreAnchorSink::OnEndEditTransaction</b> is called. When <b>ITextStoreAnchorSink::OnEndEditTransaction</b> is called, the text service will process all of the queued changes.

Use of edit transactions is optional.




## -see-also




<a href="https://msdn.microsoft.com/fb96b4fb-864f-4f32-bf7c-cf7f199e552a">ITextStoreAnchorSink</a>



<a href="https://msdn.microsoft.com/9e86d767-8ace-4bd0-af12-2139814b4e44">
        ITextStoreAnchorSink::OnStartEditTransaction
      </a>



<a href="https://msdn.microsoft.com/9ca9eac8-f30b-4a52-b851-3ad7a5c4dfb7">ITfEditTransactionSink::OnEndEditTransaction
      </a>
 

 

