---
UID: NN:d3d11sdklayers.ID3D11InfoQueue
title: ID3D11InfoQueue
author: windows-driver-content
description: An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.
old-location: direct3d11\id3d11infoqueue.htm
old-project: direct3d11
ms.assetid: 240820c7-1c1f-4e2d-8b3e-497fd931d7d2
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ID3D11InfoQueue, ID3D11InfoQueue interface [Direct3D 11], ID3D11InfoQueue interface [Direct3D 11], described, c949addb-3970-af5d-6963-d7a298716036, d3d11sdklayers/ID3D11InfoQueue, direct3d11.id3d11infoqueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d11sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11InfoQueue
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11InfoQueue interface


## -description


An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11InfoQueue</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11InfoQueue</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ca5a5e33-f912-4283-8b23-b212ace6089c">AddApplicationMessage</a>
</td>
<td align="left" width="63%">
Add a user-defined message to the message queue and send that message to debug output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7265a273-327a-482b-9d47-6931e031cff8">AddMessage</a>
</td>
<td align="left" width="63%">
Add a debug message to the message queue and send that message to debug output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/638d6af7-d425-4865-8124-dd7cd0dc6927">AddRetrievalFilterEntries</a>
</td>
<td align="left" width="63%">
Add storage filters to the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18d8a336-44aa-4a21-93c7-e6279bb51853">AddStorageFilterEntries</a>
</td>
<td align="left" width="63%">
Add storage filters to the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f56142f8-ebd6-484b-ae1f-b5c19851fbd9">ClearRetrievalFilter</a>
</td>
<td align="left" width="63%">
Remove a retrieval filter from the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26723bcf-d4c9-4c99-9e8b-fb81df18ea87">ClearStorageFilter</a>
</td>
<td align="left" width="63%">
Remove a storage filter from the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60b8e66b-84d2-4190-b503-0c8b3ed158e5">ClearStoredMessages</a>
</td>
<td align="left" width="63%">
Clear all messages from the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/747755ec-3260-4ded-9c36-efdf1a90adcb">GetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Get a message category to break on when a message with that category passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0efccfd5-55ec-4151-81ca-fe826f44adaa">GetBreakOnID</a>
</td>
<td align="left" width="63%">
Get a message identifier to break on when a message with that identifier passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4023ddb7-006f-46bc-8be8-34ee2bdd9062">GetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Get a message severity level to break on when a message with that severity level passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/685cddc5-cedd-410f-a693-665d2d69402e">GetMessage</a>
</td>
<td align="left" width="63%">
Get a message from the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/971f3158-838d-4f1c-8d3c-15dac0b6dea9">GetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Get the maximum number of messages that can be added to the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27f1b39f-b5c9-458e-a8cb-76090c240b8d">GetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Get a boolean that turns the debug output on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13e9caed-4c26-4b5e-b0c7-c6ef44ed688d">GetNumMessagesAllowedByStorageFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that were allowed to pass through a storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d49d4c7a-62a4-40ef-afdf-def3563c00fd">GetNumMessagesDeniedByStorageFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that were denied passage through a storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a2cb3c3-2b8c-47bf-b306-e13f35729686">GetNumMessagesDiscardedByMessageCountLimit</a>
</td>
<td align="left" width="63%">
Get the number of messages that were discarded due to the message count limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d07a74ed-d409-4242-9687-a61bb64e455c">GetNumStoredMessages</a>
</td>
<td align="left" width="63%">
Get the number of messages currently stored in the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0da19bef-a0b3-43d7-88e5-9270bb98b20c">GetNumStoredMessagesAllowedByRetrievalFilter</a>
</td>
<td align="left" width="63%">
Get the number of messages that are able to pass through a retrieval filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbf05fe7-91b7-40ce-895c-82e60fa456e9">GetRetrievalFilter</a>
</td>
<td align="left" width="63%">
Get the retrieval filter at the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6a50310-5c0e-450d-8ee0-48cd9531b22d">GetRetrievalFilterStackSize</a>
</td>
<td align="left" width="63%">
Get the size of the retrieval-filter stack in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87c9d6f0-8a3d-47d4-bfcb-369ec9cbf01a">GetStorageFilter</a>
</td>
<td align="left" width="63%">
Get the storage filter at the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbf17ea4-7fef-4efe-982d-9a15e16df7b1">GetStorageFilterStackSize</a>
</td>
<td align="left" width="63%">
Get the size of the storage-filter stack in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42a46071-8b2c-4e4f-9db1-2f14468346e1">PopRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pop a retrieval filter from the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ceaa5d87-50ea-4a55-b3a1-f3aa0463fb34">PopStorageFilter</a>
</td>
<td align="left" width="63%">
Pop a storage filter from the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bdbecef-9f74-4be3-8e16-e5928bbe849e">PushCopyOfRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push a copy of retrieval filter currently on the top of the retrieval-filter stack onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4538fecb-1cb6-443b-b1fe-b0e506fbecb2">PushCopyOfStorageFilter</a>
</td>
<td align="left" width="63%">
Push a copy of storage filter currently on the top of the storage-filter stack onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/906485ba-d703-4adb-8a11-f82bcf3d36ea">PushEmptyRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push an empty retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30872759-d962-4e78-9ec3-d989caf5138d">PushEmptyStorageFilter</a>
</td>
<td align="left" width="63%">
Push an empty storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba0ff492-bd35-499a-972c-135593e84fea">PushRetrievalFilter</a>
</td>
<td align="left" width="63%">
Push a retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de3f22b0-0642-4aa8-8bb0-008c1e44d3cb">PushStorageFilter</a>
</td>
<td align="left" width="63%">
Push a storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d6f66bf-01b8-4bab-a40e-98f5893050cd">SetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Set a message category to break on when a message with that category passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e245c09-bbe1-4601-826b-fe5e71ea6101">SetBreakOnID</a>
</td>
<td align="left" width="63%">
Set a message identifier to break on when a message with that identifier passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de977ab5-a277-41fe-a99d-153fa75fc15a">SetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Set a message severity level to break on when a message with that severity level passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59ed198c-65a5-4d78-867a-ba4527ad23c2">SetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Set the maximum number of messages that can be added to the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b155d2c-f7b0-4879-8086-8cccbca16a25">SetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Set a boolean that turns the debug output on or off.

</td>
</tr>
</table> 


## -remarks




            To get this interface, turn on debug layer and use <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> from the <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/100cb66a-9bf5-4d0b-9f03-ad7c00e76d9d">Layer Interfaces</a>
 

 

