---
UID: NN:textstor.ITextStoreAnchorSink
title: ITextStoreAnchorSink (textstor.h)

description: The ITextStoreAnchorSink interface is implemented by the TSF manager and is used by an anchor-based application to notify the manager when certain events occur. The manager installs this advise sink by calling ITextStoreAnchor::AdviseSink.
old-location: tsf\itextstoreanchorsink.htm
tech.root: TSF
ms.assetid: fb96b4fb-864f-4f32-bf7c-cf7f199e552a

ms.date: 12/05/2018
ms.keywords: ITextStoreAnchorSink, ITextStoreAnchorSink interface [Text Services Framework], ITextStoreAnchorSink interface [Text Services Framework],described, _tsf_itextstoreanchorsink_ref, textstor/ITextStoreAnchorSink, tsf.itextstoreanchorsink
ms.topic: interface
f1_keywords: 
 - "textstor/ITextStoreAnchorSink"
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
 - ITextStoreAnchorSink
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITextStoreAnchorSink interface


## -description


The <b>ITextStoreAnchorSink</b> interface is implemented by the TSF manager and is used by an anchor-based application to notify the manager when certain events occur. The manager installs this advise sink by calling <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-advisesink">ITextStoreAnchor::AdviseSink</a>.

The interface ID is IID_ITextStoreAnchorSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoreAnchorSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStoreAnchorSink</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onattrschange">OnAttrsChange</a>
</td>
<td align="left" width="63%">
Called when the value of one or more text attributes changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onendedittransaction">OnEndEditTransaction</a>
</td>
<td align="left" width="63%">
Called when an edit transaction is terminated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onlayoutchange">OnLayoutChange</a>
</td>
<td align="left" width="63%">
Called when the layout (on-screen representation) of the document changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onlockgranted">OnLockGranted</a>
</td>
<td align="left" width="63%">
Called to grant a document lock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onselectionchange">OnSelectionChange</a>
</td>
<td align="left" width="63%">
Called when the selection within the text stream changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onstartedittransaction">OnStartEditTransaction</a>
</td>
<td align="left" width="63%">
Called when an edit transaction is started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onstatuschange">OnStatusChange</a>
</td>
<td align="left" width="63%">
Called when the text stream status changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-ontextchange">OnTextChange</a>
</td>
<td align="left" width="63%">
Called when text in the text stream changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TSF/document-locks">Document Locks</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-advisesink">ITextStoreAnchor::AdviseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/text-stores">Text Stores</a>
 

 

