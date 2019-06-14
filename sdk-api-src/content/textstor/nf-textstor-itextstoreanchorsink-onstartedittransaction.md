---
UID: NF:textstor.ITextStoreAnchorSink.OnStartEditTransaction
title: ITextStoreAnchorSink::OnStartEditTransaction (textstor.h)
author: windows-sdk-content
description: ITextStoreAnchorSink::OnStartEditTransaction method
old-location: tsf\itextstoreanchorsink_onstartedittransaction.htm
tech.root: TSF
ms.assetid: 9e86d767-8ace-4bd0-af12-2139814b4e44
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchorSink interface [Text Services Framework],OnStartEditTransaction method, ITextStoreAnchorSink.OnStartEditTransaction, ITextStoreAnchorSink::OnStartEditTransaction, OnStartEditTransaction, OnStartEditTransaction method [Text Services Framework], OnStartEditTransaction method [Text Services Framework],ITextStoreAnchorSink interface, _tsf_itextstoreanchorsink_onstartedittransaction_ref, textstor/ITextStoreAnchorSink::OnStartEditTransaction, tsf.itextstoreanchorsink_onstartedittransaction
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
 - ITextStoreAnchorSink.OnStartEditTransaction
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
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

An edit transaction is a group of text changes that should be processed at one time. Calling this method allows a text service to queue the upcoming changes until <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onendedittransaction">ITextStoreAnchorSink::OnEndEditTransaction</a> is called. When <b>ITextStoreAnchorSink::OnEndEditTransaction</b> is called, the text service will process all queued changes.

Use of edit transactions is optional.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreanchorsink">ITextStoreAnchorSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onendedittransaction">ITextStoreAnchorSink::OnEndEditTransaction
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfedittransactionsink-onstartedittransaction">ITfEditTransactionSink::OnStartEditTransaction
      </a>
 

 

