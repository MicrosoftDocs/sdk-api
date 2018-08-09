---
UID: NN:textstor.ITextStoreACPSink
title: ITextStoreACPSink
author: windows-sdk-content
description: The ITextStoreACPSink interface is implemented by the TSF manager and is used by an ACP-based application to notify the manager when certain events occur. The manager installs this advise sink by calling ITextStoreACP::AdviseSink.
old-location: tsf\itextstoreacpsink.htm
old-project: TSF
ms.assetid: d7e5a04f-7159-436e-a522-4cb63063aeef
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextStoreACPSink, ITextStoreACPSink interface [Text Services Framework], ITextStoreACPSink interface [Text Services Framework],described, _tsf_itextstoreacpsink_ref, textstor/ITextStoreACPSink, tsf.itextstoreacpsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TsRunType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACPSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACPSink interface


## -description


The <b>ITextStoreACPSink</b> interface is implemented by the TSF manager and is used by an ACP-based application to notify the manager when certain events occur. The manager installs this advise sink by calling <a href="https://msdn.microsoft.com/aadf54e4-25ba-4280-a184-e1d2a2594c3c">ITextStoreACP::AdviseSink</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoreACPSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextStoreACPSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextStoreACPSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae1e5f92-7462-46b4-b4dd-5032147de688">OnAttrsChange</a>
</td>
<td align="left" width="63%">
Called when the value of one or more text attribute changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d2819a2-c780-47bb-b3e5-0836b8b4c5dd">OnEndEditTransaction</a>
</td>
<td align="left" width="63%">
Called when an edit transaction is terminated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2018d3ef-892f-46c0-8dd0-3e27a9f2272c">OnLayoutChange</a>
</td>
<td align="left" width="63%">
Called when the layout (on-screen representation) of the document changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddedd278-ec28-417e-bce2-cdb74db7b0f3">OnLockGranted</a>
</td>
<td align="left" width="63%">
Called to grant a document lock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/500333ae-06dc-4194-a21b-e03c1acc9f9a">OnSelectionChange</a>
</td>
<td align="left" width="63%">
Called when the selection within the document changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d5452a1-b2f3-42d6-a32d-95965c2af8d3">OnStartEditTransaction</a>
</td>
<td align="left" width="63%">
Called when an edit transaction is started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44ecc116-e6f3-48dd-9bff-16d3c1e4cc97">OnStatusChange</a>
</td>
<td align="left" width="63%">
Called when the status of the document changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed11ebb8-312b-40c7-90de-f5aa7591afd2">OnTextChange</a>
</td>
<td align="left" width="63%">
Called when the text of a document changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">Document Locks</a>



<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP
      </a>



<a href="https://msdn.microsoft.com/aadf54e4-25ba-4280-a184-e1d2a2594c3c">ITextStoreACP::AdviseSink
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/c827999a-0b74-4e5d-901e-4c2fa1d74929">Text Stores</a>
 

 

