---
UID: NN:faxcomex.IFaxIncomingMessageIterator
title: IFaxIncomingMessageIterator
author: windows-sdk-content
description: The IFaxIncomingMessageIterator interface is used by a fax client application to move through the archive of inbound fax messages that the fax service has successfully received.
old-location: fax\_mfax_faxincomingmessageiterator_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_9zg2_cpp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxIncomingMessageIterator, IFaxIncomingMessageIterator interface [Fax Service], IFaxIncomingMessageIterator interface [Fax Service],described, _mfax_faxincomingmessageiterator_cpp, fax._mfax_faxincomingmessageiterator_cpp, faxcomex/IFaxIncomingMessageIterator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxIncomingMessageIterator
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxIncomingMessageIterator interface


## -description


The <b>IFaxIncomingMessageIterator</b> interface is used by a fax client application to move through the archive of inbound fax messages that the fax service has successfully received. Because the <b>IFaxIncomingMessageIterator</b> interface is a forward iterator, you can only move forward through the archive from beginning to end, and you can access only one fax message (<a href="https://msdn.microsoft.com/29fa30c9-d4f2-4ed5-95fc-873f2263c7bb">IFaxIncomingMessage</a> object) at a time.

The <b>IFaxIncomingMessageIterator</b> interface is accessed through the <a href="https://msdn.microsoft.com/0442fc06-20b8-4608-8532-c8901832f39b">IFaxIncomingArchive</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingMessageIterator</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxIncomingMessageIterator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxIncomingMessageIterator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b266318b-d989-47bd-b905-739830153abe">MoveFirst</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b266318b-d989-47bd-b905-739830153abe">MoveFirst</a> method moves the archive cursor to the first fax message in the archive of inbound faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1afa36b2-ef4f-4391-8dc6-5e33980fd492">MoveNext</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/1afa36b2-ef4f-4391-8dc6-5e33980fd492">MoveNext</a> method moves the archive cursor to the next message in the archive of inbound faxes.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxIncomingMessageIterator</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2efe51f0-983b-4766-ba0f-b3ddb4fea2b0">AtEOF</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2efe51f0-983b-4766-ba0f-b3ddb4fea2b0">AtEOF</a> property is the end of file marker for the archive of inbound fax messages. If this property is equal to <b>TRUE</b>, the archive cursor has moved beyond the last fax message in the inbound fax archive. If this property is equal to <b>FALSE</b>, the archive cursor has not yet reached the end of the archive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/52846cf4-4e6b-43cc-a9ba-3e4820fc2aa8">Message</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/52846cf4-4e6b-43cc-a9ba-3e4820fc2aa8">Message</a> property retrieves the inbound fax message under the archive cursor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0b9280dc-5895-4c11-9298-459b7792ad39">PrefetchSize</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0b9280dc-5895-4c11-9298-459b7792ad39">PrefetchSize</a> property indicates the size of the prefetch (read-ahead) buffer.

</td>
</tr>
</table> 


## -remarks



To create a <b>FaxIncomingMessageIterator</b> object in C++, call the <a href="https://msdn.microsoft.com/7b314907-97c9-49f8-abaf-d716706c6b79">IFaxIncomingArchive::GetMessages</a> method.




## -see-also




<a href="https://msdn.microsoft.com/0969319b-7846-44a0-9667-161b326acea6">FaxIncomingMessageIterator</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/0442fc06-20b8-4608-8532-c8901832f39b">IFaxIncomingArchive</a>
 

 

