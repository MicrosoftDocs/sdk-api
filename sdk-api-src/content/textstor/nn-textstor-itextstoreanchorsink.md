---
UID: NN:textstor.ITextStoreAnchorSink
title: ITextStoreAnchorSink
author: windows-sdk-content
description: The ITextStoreAnchorSink interface is implemented by the TSF manager and is used by an anchor-based application to notify the manager when certain events occur. The manager installs this advise sink by calling ITextStoreAnchor::AdviseSink.
old-location: tsf\itextstoreanchorsink.htm
tech.root: TSF
ms.assetid: fb96b4fb-864f-4f32-bf7c-cf7f199e552a
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITextStoreAnchorSink, ITextStoreAnchorSink interface [Text Services Framework], ITextStoreAnchorSink interface [Text Services Framework],described, _tsf_itextstoreanchorsink_ref, textstor/ITextStoreAnchorSink, tsf.itextstoreanchorsink
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITextStoreAnchorSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchorSink interface


## -description


The <b>ITextStoreAnchorSink</b> interface is implemented by the TSF manager and is used by an anchor-based application to notify the manager when certain events occur. The manager installs this advise sink by calling <a href="https://msdn.microsoft.com/a2196d1c-b03e-44b4-b695-970feddb8ce5">ITextStoreAnchor::AdviseSink</a>.

The interface ID is IID_ITextStoreAnchorSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoreAnchorSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextStoreAnchorSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextStoreAnchorSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa7226dd-1d4a-44ed-94b7-b93813bca2f8">OnAttrsChange</a>
</td>
<td align="left" width="63%">
Called when the value of one or more text attributes changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe7610b3-02f0-491a-8c55-f9dc9843073b">OnEndEditTransaction</a>
</td>
<td align="left" width="63%">
Called when an edit transaction is terminated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22629ca6-5701-4f6f-b797-bb71c8d31da6">OnLayoutChange</a>
</td>
<td align="left" width="63%">
Called when the layout (on-screen representation) of the document changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a2ab828-1eb8-4aae-bebd-dc8b406fd58f">OnLockGranted</a>
</td>
<td align="left" width="63%">
Called to grant a document lock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e33932b0-f5ce-4325-809d-ec06cb4a49a6">OnSelectionChange</a>
</td>
<td align="left" width="63%">
Called when the selection within the text stream changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e86d767-8ace-4bd0-af12-2139814b4e44">OnStartEditTransaction</a>
</td>
<td align="left" width="63%">
Called when an edit transaction is started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28bdfa93-29c1-4a9f-b85e-20c39a1b429b">OnStatusChange</a>
</td>
<td align="left" width="63%">
Called when the text stream status changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bdf12bc-c15e-4bdb-8bc0-53172e9c943e">OnTextChange</a>
</td>
<td align="left" width="63%">
Called when text in the text stream changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">Document Locks</a>



<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor
      </a>



<a href="https://msdn.microsoft.com/a2196d1c-b03e-44b4-b695-970feddb8ce5">ITextStoreAnchor::AdviseSink
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/c827999a-0b74-4e5d-901e-4c2fa1d74929">Text Stores</a>
 

 

