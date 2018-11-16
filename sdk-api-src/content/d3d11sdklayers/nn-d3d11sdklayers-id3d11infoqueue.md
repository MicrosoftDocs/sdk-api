---
UID: NN:d3d11sdklayers.ID3D11InfoQueue
title: ID3D11InfoQueue
author: windows-sdk-content
description: An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.
old-location: direct3d11\id3d11infoqueue.htm
tech.root: direct3d11
ms.assetid: 240820c7-1c1f-4e2d-8b3e-497fd931d7d2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D11InfoQueue, ID3D11InfoQueue interface [Direct3D 11], ID3D11InfoQueue interface [Direct3D 11],described, c949addb-3970-af5d-6963-d7a298716036, d3d11sdklayers/ID3D11InfoQueue, direct3d11.id3d11infoqueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11InfoQueue interface


## -description


An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11InfoQueue</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D11InfoQueue</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Ff476539(v=VS.85).aspx">AddApplicationMessage</a>
</td>
<td align="left" width="63%">
Add a user-defined message to the message queue and send that message to debug output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476540(v=VS.85).aspx">AddMessage</a>
</td>
<td align="left" width="63%">
Add a debug message to the message queue and send that message to debug output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476541(v=VS.85).aspx">AddRetrievalFilterEntries</a>
</td>
<td align="left" width="63%">
Add storage filters to the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476542(v=VS.85).aspx">AddStorageFilterEntries</a>
</td>
<td align="left" width="63%">
Add storage filters to the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476543(v=VS.85).aspx">ClearRetrievalFilter</a>
</td>
<td align="left" width="63%">
Remove a retrieval filter from the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476544(v=VS.85).aspx">ClearStorageFilter</a>
</td>
<td align="left" width="63%">
Remove a storage filter from the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476545(v=VS.85).aspx">ClearStoredMessages</a>
</td>
<td align="left" width="63%">
Clear all messages from the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476546(v=VS.85).aspx">GetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Get a message category to break on when a message with that category passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476547(v=VS.85).aspx">GetBreakOnID</a>
</td>
<td align="left" width="63%">
Get a message identifier to break on when a message with that identifier passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476548(v=VS.85).aspx">GetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Get a message severity level to break on when a message with that severity level passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476549(v=VS.85).aspx">GetMessage</a>
</td>
<td align="left" width="63%">
Get a message from the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476550(v=VS.85).aspx">GetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Get the maximum number of messages that can be added to the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476551(v=VS.85).aspx">GetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Get a boolean that turns the debug output on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476552(v=VS.85).aspx">GetNumMessagesAllowedByStorageFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that were allowed to pass through a storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476553(v=VS.85).aspx">GetNumMessagesDeniedByStorageFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that were denied passage through a storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476554(v=VS.85).aspx">GetNumMessagesDiscardedByMessageCountLimit</a>
</td>
<td align="left" width="63%">
Get the number of messages that were discarded due to the message count limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476556(v=VS.85).aspx">GetNumStoredMessages</a>
</td>
<td align="left" width="63%">
Get the number of messages currently stored in the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476557(v=VS.85).aspx">GetNumStoredMessagesAllowedByRetrievalFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that are able to pass through a retrieval filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476558(v=VS.85).aspx">GetRetrievalFilter</a>
</td>
<td align="left" width="63%">
Get the retrieval filter at the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476559(v=VS.85).aspx">GetRetrievalFilterStackSize</a>
</td>
<td align="left" width="63%">
Get the size of the retrieval-filter stack in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476560(v=VS.85).aspx">GetStorageFilter</a>
</td>
<td align="left" width="63%">
Get the storage filter at the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476561(v=VS.85).aspx">GetStorageFilterStackSize</a>
</td>
<td align="left" width="63%">
Get the size of the storage-filter stack in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476562(v=VS.85).aspx">PopRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pop a retrieval filter from the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476563(v=VS.85).aspx">PopStorageFilter</a>
</td>
<td align="left" width="63%">
Pop a storage filter from the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476564(v=VS.85).aspx">PushCopyOfRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push a copy of retrieval filter currently on the top of the retrieval-filter stack onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476565(v=VS.85).aspx">PushCopyOfStorageFilter</a>
</td>
<td align="left" width="63%">
Push a copy of storage filter currently on the top of the storage-filter stack onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476566(v=VS.85).aspx">PushEmptyRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push an empty retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476567(v=VS.85).aspx">PushEmptyStorageFilter</a>
</td>
<td align="left" width="63%">
Push an empty storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476568(v=VS.85).aspx">PushRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push a retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476569(v=VS.85).aspx">PushStorageFilter</a>
</td>
<td align="left" width="63%">
Push a storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476570(v=VS.85).aspx">SetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Set a message category to break on when a message with that category passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476571(v=VS.85).aspx">SetBreakOnID</a>
</td>
<td align="left" width="63%">
Set a message identifier to break on when a message with that identifier passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476572(v=VS.85).aspx">SetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Set a message severity level to break on when a message with that severity level passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476573(v=VS.85).aspx">SetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Set the maximum number of messages that can be added to the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476574(v=VS.85).aspx">SetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Set a boolean that turns the debug output on or off.

</td>
</tr>
</table> 


## -remarks



To get this interface, turn on debug layer and use <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> from the <a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476158(v=VS.85).aspx">Layer Interfaces</a>
 

 

