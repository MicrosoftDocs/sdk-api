---
UID: NN:textstor.ITextStoreACPSink
title: ITextStoreACPSink (textstor.h)
description: The ITextStoreACPSink interface is implemented by the TSF manager and is used by an ACP-based application to notify the manager when certain events occur. The manager installs this advise sink by calling ITextStoreACP::AdviseSink.helpviewer_keywords: ["ITextStoreACPSink","ITextStoreACPSink interface [Text Services Framework]","ITextStoreACPSink interface [Text Services Framework]","described","_tsf_itextstoreacpsink_ref","textstor/ITextStoreACPSink","tsf.itextstoreacpsink"]
old-location: tsf\itextstoreacpsink.htm
tech.root: TSF
ms.assetid: d7e5a04f-7159-436e-a522-4cb63063aeef
ms.date: 12/05/2018
ms.keywords: ITextStoreACPSink, ITextStoreACPSink interface [Text Services Framework], ITextStoreACPSink interface [Text Services Framework],described, _tsf_itextstoreacpsink_ref, textstor/ITextStoreACPSink, tsf.itextstoreacpsink
f1_keywords:
- textstor/ITextStoreACPSink
dev_langs:
- c++
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
- ITextStoreACPSink
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITextStoreACPSink interface


## -description


The <b>ITextStoreACPSink</b> interface is implemented by the TSF manager and is used by an ACP-based application to notify the manager when certain events occur. The manager installs this advise sink by calling <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-advisesink">ITextStoreACP::AdviseSink</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoreACPSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStoreACPSink</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onattrschange">OnAttrsChange</a>
</td>
<td align="left" width="63%">
Called when the value of one or more text attribute changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onendedittransaction">OnEndEditTransaction</a>
</td>
<td align="left" width="63%">
Called when an edit transaction is terminated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onlayoutchange">OnLayoutChange</a>
</td>
<td align="left" width="63%">
Called when the layout (on-screen representation) of the document changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onlockgranted">OnLockGranted</a>
</td>
<td align="left" width="63%">
Called to grant a document lock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onselectionchange">OnSelectionChange</a>
</td>
<td align="left" width="63%">
Called when the selection within the document changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onstartedittransaction">OnStartEditTransaction</a>
</td>
<td align="left" width="63%">
Called when an edit transaction is started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-onstatuschange">OnStatusChange</a>
</td>
<td align="left" width="63%">
Called when the status of the document changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-ontextchange">OnTextChange</a>
</td>
<td align="left" width="63%">
Called when the text of a document changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TSF/document-locks">Document Locks</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-advisesink">ITextStoreACP::AdviseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/text-stores">Text Stores</a>
 

 

