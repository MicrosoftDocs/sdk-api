---
UID: NN:faxcomex.IFaxOutgoingMessageIterator
title: IFaxOutgoingMessageIterator (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutgoingMessageIterator interface describes an object that is used by a fax client application to move through the archive of fax messages that the fax service has successfully transmitted, represented by FaxOutgoingMessage objects.
old-location: fax\_mfax_faxoutgoingmessageiterator_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8euq_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingMessageIterator, IFaxOutgoingMessageIterator interface [Fax Service], IFaxOutgoingMessageIterator interface [Fax Service],described, _mfax_faxoutgoingmessageiterator_cpp, fax._mfax_faxoutgoingmessageiterator_cpp, faxcomex/IFaxOutgoingMessageIterator
ms.topic: interface
f1_keywords: ["faxcomex/IFaxOutgoingMessageIterator"]
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingMessageIterator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxOutgoingMessageIterator interface


## -description


The <b>IFaxOutgoingMessageIterator</b> interface describes an object that is used by a fax client application to move through the archive of fax messages that the fax service has successfully transmitted, represented by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessage">FaxOutgoingMessage</a> objects. Because the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator">FaxOutgoingMessageIterator</a> object is a forward iterator, you can only move forward through the archive, from beginning to end, and you can access only one message at a time.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingMessageIterator</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxOutgoingMessageIterator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxOutgoingMessageIterator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator-movefirst-vb">MoveFirst</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator-movefirst-vb">IFaxOutgoingMessageIterator::MoveFirst</a> method moves the archive cursor to the first fax message in the outbound archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator-movenext-vb">MoveNext</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator-movenext-vb">IFaxOutgoingMessageIterator::MoveNext</a> method moves the archive cursor to the next fax message in the outbound archive.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingMessageIterator</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator-ateof-vb">AtEOF</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The AtEOF property is the end-of-file marker for the archive of outbound fax messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutgoingmessageiterator-get_message">Message</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxoutgoingmessageiterator-get_message">IFaxOutgoingMessageIterator::get_Message</a> property retrieves the outbound fax message under the archive cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator-prefetchsize-vb">PrefetchSize</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator-prefetchsize-vb">IFaxOutgoingMessageIterator::get_PrefetchSize</a> property indicates the size of the prefetch (read-ahead) buffer. This determines how many fax messages the iterator object retrieves from the fax server when the object needs to refresh its contents.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutgoingMessageIterator</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxoutgoingmessageiterator">FaxOutgoingMessageIterator</a> object.



