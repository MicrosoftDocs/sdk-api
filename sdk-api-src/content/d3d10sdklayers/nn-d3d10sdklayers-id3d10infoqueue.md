---
UID: NN:d3d10sdklayers.ID3D10InfoQueue
title: ID3D10InfoQueue
author: windows-sdk-content
description: An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.
old-location: direct3d10\id3d10infoqueue.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 1ef0bd38-23d3-fa53-cf27-ff502bb674f2, ID3D10InfoQueue, ID3D10InfoQueue interface [Direct3D 10], ID3D10InfoQueue interface [Direct3D 10],described, d3d10sdklayers/ID3D10InfoQueue, direct3d10.id3d10infoqueue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10sdklayers.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10InfoQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10InfoQueue interface


## -description


An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10InfoQueue</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10InfoQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10InfoQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/223f9a01-4507-4877-bd86-c5b9cb441d7a">AddApplicationMessage</a>
</td>
<td align="left" width="63%">
Add a user-defined message to the message queue and send that message to debug output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d31a0c87-b895-49e2-96e6-1df68db3995b">AddMessage</a>
</td>
<td align="left" width="63%">
Add a Direct3D 10 debug message to the message queue and send that message to debug output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9f9e6a9-abf7-413d-9c1d-cc68a6fe9ff8">AddRetrievalFilterEntries</a>
</td>
<td align="left" width="63%">
Add storage filters to the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/803707c5-fe5a-41ed-a980-8b0c6f258724">AddStorageFilterEntries</a>
</td>
<td align="left" width="63%">
Add storage filters to the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/496a9b9e-c68d-4a05-928c-beb0d1a36396">ClearRetrievalFilter</a>
</td>
<td align="left" width="63%">
Remove a retrieval filter from the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b842887b-9dba-4f52-9937-5aba8651a883">ClearStorageFilter</a>
</td>
<td align="left" width="63%">
Remove a storage filter from the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2334a06f-79a8-4f84-9bed-a16f706630c8">ClearStoredMessages</a>
</td>
<td align="left" width="63%">
Clear all messages from the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3118e72-e8ee-4edc-bc42-d0f179e7fd94">GetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Get a message category to break on when a message with that category passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7932169-3acc-431c-8cb5-96970aa8006f">GetBreakOnID</a>
</td>
<td align="left" width="63%">
Get a message identifier to break on when a message with that identifier passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b08b4e39-6f6b-4b3e-9b40-d113c426d7a7">GetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Get a message severity level to break on when a message with that severity level passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7ed2819-d726-4719-b46c-03c001b9b40d">GetMessage</a>
</td>
<td align="left" width="63%">
Get a message from the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54821cbf-a950-4403-b39c-9c89635336d2">GetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Get the maximum number of messages that can be added to the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4687944e-160d-412f-b306-80222e849648">GetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Get a boolean that turns the debug output on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a43e6f16-aa87-4eb6-9b6e-d3e94af62dd8">GetNumMessagesAllowedByStorageFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that were allowed to pass through a storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6abaa90d-146a-4266-ab93-13c45a0048bb">GetNumMessagesDeniedByStorageFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that were denied passage through a storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20b7f033-d7ed-469c-8628-de6229fdc294">GetNumMessagesDiscardedByMessageCountLimit</a>
</td>
<td align="left" width="63%">
Get the number of messages that were discarded due to the message count limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df3a5504-8b27-406e-840c-4a85e499cddc">GetNumStoredMessages</a>
</td>
<td align="left" width="63%">
Get the number of messages currently stored in the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7f759b0-d5ee-4777-a16a-315baa09766c">GetNumStoredMessagesAllowedByRetrievalFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that are able to pass through a retrieval filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9868e103-56c1-4425-b5ba-ee8a4ba71b6b">GetRetrievalFilter</a>
</td>
<td align="left" width="63%">
Get the retrieval filter at the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/936e7e2e-54a1-4db5-8080-d9afdaad7a0d">GetRetrievalFilterStackSize</a>
</td>
<td align="left" width="63%">
Get the size of the retrieval-filter stack in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5739e222-545b-46bc-93c7-d5fa5e91437e">GetStorageFilter</a>
</td>
<td align="left" width="63%">
Get the storage filter at the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e7aafa8-99d9-49bc-9d15-ad3ecd50f89d">GetStorageFilterStackSize</a>
</td>
<td align="left" width="63%">
Get the size of the storage-filter stack in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab1b2690-a2c8-4441-bc3c-24c7fa5501d5">PopRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pop a retrieval filter from the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e5a1bbf-5969-4ff4-84bd-42cc3a46dc0f">PopStorageFilter</a>
</td>
<td align="left" width="63%">
Pop a storage filter from the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5abc6c37-c66b-4727-b964-de7b40adf71d">PushCopyOfRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push a copy of retrieval filter currently on the top of the retrieval-filter stack onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f216e4a4-ef11-4d29-805e-36e53d65c602">PushCopyOfStorageFilter</a>
</td>
<td align="left" width="63%">
Push a copy of storage filter currently on the top of the storage-filter stack onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/177f714b-2df2-415c-a0b0-e1e68200ac57">PushEmptyRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push an empty retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd5c9a7c-885a-4d8a-8581-d89e1bce722c">PushEmptyStorageFilter</a>
</td>
<td align="left" width="63%">
Push an empty storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad609c71-7683-4745-b23b-40db341e57db">PushRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push a retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a54d6c4-6f05-46dd-a8e1-0071fb68e42a">PushStorageFilter</a>
</td>
<td align="left" width="63%">
Push a storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc7611fc-3f32-49f0-ac5a-28148b257ab3">SetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Set a message category to break on when a message with that category passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/759b6f11-253a-43eb-a773-5fc6f03c0227">SetBreakOnID</a>
</td>
<td align="left" width="63%">
Set a message identifier to break on when a message with that identifier passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39b2706c-9cc8-4195-b7d4-673a226d21d7">SetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Set a message severity level to break on when a message with that severity level passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23767ef0-d87c-4ef9-a2d5-d970832f6d4e">SetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Set the maximum number of messages that can be added to the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c695806-a866-4446-89d7-cc8ac860a490">SetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Set a boolean that turns the debug output on or off.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by turning on the <a href="https://msdn.microsoft.com/19c81383-6ac7-49ea-98a3-bf761a32ab40">debug layer</a> and querying it from the <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a> using <a href="http://msdn.microsoft.com/en-us/library/ms682521(VS.85).aspx">IUnknown::QueryInterface</a>.


```
hr = D3D10CreateDeviceAndSwapChain( NULL, g_driverType, NULL, D3D10_CREATE_DEVICE_DEBUG, D3D10_SDK_VERSION, &sd, &g_pSwapChain, &g_pd3dDevice );
...
ID3D10InfoQueue * infoQueue;
g_pd3dDevice->QueryInterface(__uuidof(ID3D10InfoQueue),  (void **)&infoQueue); 

```





## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>
 

 

