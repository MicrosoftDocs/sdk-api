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

# IFaxOutgoingMessageIterator interface


## -description


The <b>IFaxOutgoingMessageIterator</b> interface describes an object that is used by a fax client application to move through the archive of fax messages that the fax service has successfully transmitted, represented by <a href="https://msdn.microsoft.com/fb06254f-f37b-4783-b4fd-42b5c5a28496">FaxOutgoingMessage</a> objects. Because the <a href="https://msdn.microsoft.com/4eab8319-23ff-4f25-9402-bcb53a440879">FaxOutgoingMessageIterator</a> object is a forward iterator, you can only move forward through the archive, from beginning to end, and you can access only one message at a time.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxOutgoingMessageIterator</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxOutgoingMessageIterator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e1bc35d2-5c0c-48fe-9e89-ffeb7cacc2db">MoveFirst</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/e1bc35d2-5c0c-48fe-9e89-ffeb7cacc2db">IFaxOutgoingMessageIterator::MoveFirst</a> method moves the archive cursor to the first fax message in the outbound archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46a2021f-170f-41db-ba4a-b7bd4b4c9951">MoveNext</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/46a2021f-170f-41db-ba4a-b7bd4b4c9951">IFaxOutgoingMessageIterator::MoveNext</a> method moves the archive cursor to the next fax message in the outbound archive.

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

<a href="https://msdn.microsoft.com/f4b4bfbd-041a-4495-8d4e-fcb81b83bb7e">AtEOF</a>


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

<a href="https://msdn.microsoft.com/36c7a524-2d95-4afd-a8e1-479007196e9b">Message</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/36c7a524-2d95-4afd-a8e1-479007196e9b">IFaxOutgoingMessageIterator::get_Message</a> property retrieves the outbound fax message under the archive cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/101f2c77-50e1-4ed4-ae01-d52a21abaaf2">PrefetchSize</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/101f2c77-50e1-4ed4-ae01-d52a21abaaf2">IFaxOutgoingMessageIterator::get_PrefetchSize</a> property indicates the size of the prefetch (read-ahead) buffer. This determines how many fax messages the iterator object retrieves from the fax server when the object needs to refresh its contents.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxOutgoingMessageIterator</b> is provided as the <a href="https://msdn.microsoft.com/4eab8319-23ff-4f25-9402-bcb53a440879">FaxOutgoingMessageIterator</a> object.



