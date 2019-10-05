---
UID: NN:d3d11sdklayers.ID3D11InfoQueue
title: ID3D11InfoQueue (d3d11sdklayers.h)
author: windows-sdk-content
description: An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.
old-location: direct3d11\id3d11infoqueue.htm
tech.root: direct3d11
ms.assetid: 240820c7-1c1f-4e2d-8b3e-497fd931d7d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11InfoQueue, ID3D11InfoQueue interface [Direct3D 11], ID3D11InfoQueue interface [Direct3D 11],described, c949addb-3970-af5d-6963-d7a298716036, d3d11sdklayers/ID3D11InfoQueue, direct3d11.id3d11infoqueue
ms.topic: interface
f1_keywords: 
 - "d3d11sdklayers/ID3D11InfoQueue"
dev_langs:
 - c++
req.header: d3d11sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InfoQueue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11InfoQueue interface


## -description


An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11InfoQueue</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11InfoQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11InfoQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-addapplicationmessage">AddApplicationMessage</a>
</td>
<td align="left" width="63%">
Add a user-defined message to the message queue and send that message to debug output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage">AddMessage</a>
</td>
<td align="left" width="63%">
Add a debug message to the message queue and send that message to debug output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-addretrievalfilterentries">AddRetrievalFilterEntries</a>
</td>
<td align="left" width="63%">
Add storage filters to the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-addstoragefilterentries">AddStorageFilterEntries</a>
</td>
<td align="left" width="63%">
Add storage filters to the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-clearretrievalfilter">ClearRetrievalFilter</a>
</td>
<td align="left" width="63%">
Remove a retrieval filter from the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-clearstoragefilter">ClearStorageFilter</a>
</td>
<td align="left" width="63%">
Remove a storage filter from the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-clearstoredmessages">ClearStoredMessages</a>
</td>
<td align="left" width="63%">
Clear all messages from the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getbreakoncategory">GetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Get a message category to break on when a message with that category passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getbreakonid">GetBreakOnID</a>
</td>
<td align="left" width="63%">
Get a message identifier to break on when a message with that identifier passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getbreakonseverity">GetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Get a message severity level to break on when a message with that severity level passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage">GetMessage</a>
</td>
<td align="left" width="63%">
Get a message from the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getmessagecountlimit">GetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Get the maximum number of messages that can be added to the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getmutedebugoutput">GetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Get a boolean that turns the debug output on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getnummessagesallowedbystoragefilter">GetNumMessagesAllowedByStorageFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that were allowed to pass through a storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getnummessagesdeniedbystoragefilter">GetNumMessagesDeniedByStorageFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that were denied passage through a storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getnummessagesdiscardedbymessagecountlimit">GetNumMessagesDiscardedByMessageCountLimit</a>
</td>
<td align="left" width="63%">
Get the number of messages that were discarded due to the message count limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getnumstoredmessages">GetNumStoredMessages</a>
</td>
<td align="left" width="63%">
Get the number of messages currently stored in the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getnumstoredmessagesallowedbyretrievalfilter">GetNumStoredMessagesAllowedByRetrievalFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that are able to pass through a retrieval filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getretrievalfilter">GetRetrievalFilter</a>
</td>
<td align="left" width="63%">
Get the retrieval filter at the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getretrievalfilterstacksize">GetRetrievalFilterStackSize</a>
</td>
<td align="left" width="63%">
Get the size of the retrieval-filter stack in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getstoragefilter">GetStorageFilter</a>
</td>
<td align="left" width="63%">
Get the storage filter at the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getstoragefilterstacksize">GetStorageFilterStackSize</a>
</td>
<td align="left" width="63%">
Get the size of the storage-filter stack in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-popretrievalfilter">PopRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pop a retrieval filter from the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-popstoragefilter">PopStorageFilter</a>
</td>
<td align="left" width="63%">
Pop a storage filter from the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-pushcopyofretrievalfilter">PushCopyOfRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push a copy of retrieval filter currently on the top of the retrieval-filter stack onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-pushcopyofstoragefilter">PushCopyOfStorageFilter</a>
</td>
<td align="left" width="63%">
Push a copy of storage filter currently on the top of the storage-filter stack onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-pushemptyretrievalfilter">PushEmptyRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push an empty retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-pushemptystoragefilter">PushEmptyStorageFilter</a>
</td>
<td align="left" width="63%">
Push an empty storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-pushretrievalfilter">PushRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push a retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-pushstoragefilter">PushStorageFilter</a>
</td>
<td align="left" width="63%">
Push a storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-setbreakoncategory">SetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Set a message category to break on when a message with that category passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-setbreakonid">SetBreakOnID</a>
</td>
<td align="left" width="63%">
Set a message identifier to break on when a message with that identifier passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-setbreakonseverity">SetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Set a message severity level to break on when a message with that severity level passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-setmessagecountlimit">SetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Set the maximum number of messages that can be added to the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-setmutedebugoutput">SetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Set a boolean that turns the debug output on or off.

</td>
</tr>
</table> 


## -remarks



To get this interface, turn on debug layer and use <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a> from the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-interfaces">Layer Interfaces</a>
 

 

