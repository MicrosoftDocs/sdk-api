---
UID: NN:d3d12sdklayers.ID3D12InfoQueue
title: ID3D12InfoQueue (d3d12sdklayers.h)
description: An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.
old-location: direct3d12\id3d12infoqueue.htm
tech.root: direct3d12
ms.assetid: 61667AAC-05AC-4745-8992-E9377641D411
ms.date: 12/05/2018
ms.keywords: ID3D12InfoQueue, ID3D12InfoQueue interface, ID3D12InfoQueue interface,described, d3d12sdklayers/ID3D12InfoQueue, direct3d12.id3d12infoqueue
f1_keywords:
- d3d12sdklayers/ID3D12InfoQueue
dev_langs:
- c++
req.header: d3d12sdklayers.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d12sdklayers.h
api_name:
- ID3D12InfoQueue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12InfoQueue interface


## -description


An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12InfoQueue</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12InfoQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12InfoQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addapplicationmessage">AddApplicationMessage</a>
</td>
<td align="left" width="63%">
Adds a user-defined message to the message queue and sends that message to debug output.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage">AddMessage</a>
</td>
<td align="left" width="63%">
Adds a debug message to the message queue and sends that message to debug output.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addretrievalfilterentries">AddRetrievalFilterEntries</a>
</td>
<td align="left" width="63%">
Add storage filters to the top of the retrieval-filter stack.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addstoragefilterentries">AddStorageFilterEntries</a>
</td>
<td align="left" width="63%">
Add storage filters to the top of the storage-filter stack.


        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-clearretrievalfilter">ClearRetrievalFilter</a>
</td>
<td align="left" width="63%">
Remove a retrieval filter from the top of the retrieval-filter stack.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-clearstoragefilter">ClearStorageFilter</a>
</td>
<td align="left" width="63%">
Remove a storage filter from the top of the storage-filter stack.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-clearstoredmessages">ClearStoredMessages</a>
</td>
<td align="left" width="63%">
Clear all messages from the message queue.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getbreakoncategory">GetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Get a message category to break on when a message with that category passes through the storage filter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getbreakonid">GetBreakOnID</a>
</td>
<td align="left" width="63%">
Get a message identifier to break on when a message with that identifier passes through the storage filter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getbreakonseverity">GetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Get a message severity level to break on when a message with that severity level passes through the storage filter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage">GetMessage</a>
</td>
<td align="left" width="63%">
Get a message from the message queue.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessagecountlimit">GetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Get the maximum number of messages that can be added to the message queue.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmutedebugoutput">GetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Get a boolean that determines if debug output is on or off.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getnummessagesallowedbystoragefilter">GetNumMessagesAllowedByStorageFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that were allowed to pass through a storage filter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getnummessagesdeniedbystoragefilter">GetNumMessagesDeniedByStorageFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that were denied passage through a storage filter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getnummessagesdiscardedbymessagecountlimit">GetNumMessagesDiscardedByMessageCountLimit</a>
</td>
<td align="left" width="63%">
Get the number of messages that were discarded due to the message count limit.


        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getnumstoredmessages">GetNumStoredMessages</a>
</td>
<td align="left" width="63%">
Get the number of messages currently stored in the message queue.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getnumstoredmessagesallowedbyretrievalfilter">GetNumStoredMessagesAllowedByRetrievalFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that are able to pass through a retrieval filter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getretrievalfilter">GetRetrievalFilter</a>
</td>
<td align="left" width="63%">
Get the retrieval filter at the top of the retrieval-filter stack.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getretrievalfilterstacksize">GetRetrievalFilterStackSize</a>
</td>
<td align="left" width="63%">
Get the size of the retrieval-filter stack in bytes.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getstoragefilter">GetStorageFilter</a>
</td>
<td align="left" width="63%">
Get the storage filter at the top of the storage-filter stack.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getstoragefilterstacksize">GetStorageFilterStackSize</a>
</td>
<td align="left" width="63%">
Get the size of the storage-filter stack in bytes.


        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-popretrievalfilter">PopRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pop a retrieval filter from the top of the retrieval-filter stack.


        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-popstoragefilter">PopStorageFilter</a>
</td>
<td align="left" width="63%">
Pop a storage filter from the top of the storage-filter stack.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-pushcopyofretrievalfilter">PushCopyOfRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push a copy of retrieval filter currently on the top of the retrieval-filter stack onto the retrieval-filter stack.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-pushcopyofstoragefilter">PushCopyOfStorageFilter</a>
</td>
<td align="left" width="63%">
Push a copy of storage filter currently on the top of the storage-filter stack onto the storage-filter stack.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-pushemptyretrievalfilter">PushEmptyRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push an empty retrieval filter onto the retrieval-filter stack.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-pushemptystoragefilter">PushEmptyStorageFilter</a>
</td>
<td align="left" width="63%">
Push an empty storage filter onto the storage-filter stack.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-pushretrievalfilter">PushRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push a retrieval filter onto the retrieval-filter stack.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-pushstoragefilter">PushStorageFilter</a>
</td>
<td align="left" width="63%">
Push a storage filter onto the storage-filter stack.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-setbreakoncategory">SetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Set a message category to break on when a message with that category passes through the storage filter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-setbreakonid">SetBreakOnID</a>
</td>
<td align="left" width="63%">
Set a message identifier to break on when a message with that identifier passes through the storage filter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-setbreakonseverity">SetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Set a message severity level to break on when a message with that severity level passes through the storage filter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-setmessagecountlimit">SetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Set the maximum number of messages that can be added to the message queue.


        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-setmutedebugoutput">SetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Set a boolean that turns the debug output on or off.



</td>
</tr>
</table> 


## -remarks



This interface is obtained by querying it from the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a> using <code>IUnknown::QueryInterface</code>. 






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-sdklayers-interfaces">Debug Layer Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

