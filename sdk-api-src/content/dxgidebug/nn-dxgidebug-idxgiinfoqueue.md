---
UID: NN:dxgidebug.IDXGIInfoQueue
title: IDXGIInfoQueue
author: windows-sdk-content
description: This interface controls the debug information queue, and can only be used if the debug layer is turned on.
old-location: direct3ddxgi\idxgiinfoqueue.htm
old-project: direct3ddxgi
ms.assetid: F1BC6752-F334-4E8C-BE42-B731635A799D
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IDXGIInfoQueue, IDXGIInfoQueue interface [DXGI], IDXGIInfoQueue interface [DXGI],described, direct3ddxgi.idxgiinfoqueue, dxgidebug/IDXGIInfoQueue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: DXGI_INFO_QUEUE_MESSAGE_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIInfoQueue
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIInfoQueue interface


## -description


This interface controls the debug information queue, and can only be used if the debug layer is turned on.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIInfoQueue</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDXGIInfoQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIInfoQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30245BF0-C0AF-4780-A55F-D55A331427FA">AddApplicationMessage</a>
</td>
<td align="left" width="63%">
Adds a user-defined message to the message queue and sends that message to the debug output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/965DA310-D082-4970-BCD1-F15F44C074D0">AddMessage</a>
</td>
<td align="left" width="63%">
Adds a debug message to the message queue and sends that message to the debug output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D93CB421-6684-4E84-B7FF-7911496078CC">AddRetrievalFilterEntries</a>
</td>
<td align="left" width="63%">
Adds retrieval filters to the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34FC5AE3-7B72-4480-ACFA-53C7FB5425DA">AddStorageFilterEntries</a>
</td>
<td align="left" width="63%">
Adds storage filters to the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F8CCB852-4719-4A1D-A881-5A9EF37E18CF">ClearRetrievalFilter</a>
</td>
<td align="left" width="63%">
Removes a retrieval filter from the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4CD81C2B-53F2-4046-A001-72CBFD5C04CA">ClearStorageFilter</a>
</td>
<td align="left" width="63%">
Removes a storage filter from the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DAE3D3F2-A07E-4A24-863A-042AB3DAF98E">ClearStoredMessages</a>
</td>
<td align="left" width="63%">
Clears all messages from the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12099FA2-2801-45E7-98C3-5A29F5764B8D">GetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Determines whether the break on a message category is turned on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A7DF79E0-137D-4CBD-AD03-B9BC4532D60F">GetBreakOnID</a>
</td>
<td align="left" width="63%">
Determines whether the break on a message identifier is turned on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0E03ABE8-02BC-4721-B92C-87DA5D52D0AD">GetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Determines whether the break on a message severity level is turned on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/208C3253-09AE-4379-808D-BA0BECC59BF8">GetMessage</a>
</td>
<td align="left" width="63%">
Gets a message from the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F9700374-255D-423E-8E60-4FE7FFA9E807">GetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Gets the maximum number of messages that can be added to the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8123DE14-31C1-4304-A295-C7D0C3633C36">GetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Determines whether the debug output is turned on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B838A0D9-6888-46BF-AE18-8C3546535037">GetNumMessagesAllowedByStorageFilter</a>
</td>
<td align="left" width="63%">
Gets the number of messages that a storage filter allowed to pass through.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98A71D07-8E9A-403D-B02B-70B7F4112246">GetNumMessagesDeniedByStorageFilter</a>
</td>
<td align="left" width="63%">
Gets the number of messages that were denied passage through a storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8F97E69B-5534-409F-9702-9FC6D7940D65">GetNumMessagesDiscardedByMessageCountLimit</a>
</td>
<td align="left" width="63%">
Gets the number of messages that were discarded due to the message count limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81556BB3-D8B8-4868-8B21-C9E01C3F183E">GetNumStoredMessages</a>
</td>
<td align="left" width="63%">
Gets the number of messages currently stored in the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1BFFEE9F-7902-41B7-9607-BD0E955FBD8B">GetNumStoredMessagesAllowedByRetrievalFilters</a>
</td>
<td align="left" width="63%">
Gets the number of messages that can pass through a retrieval filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95907EF0-858B-4CDF-A112-6E59138769BD">GetRetrievalFilter</a>
</td>
<td align="left" width="63%">
Gets the retrieval filter at the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E5173EC8-483D-4A90-BDF0-7A7D115A0CF9">GetRetrievalFilterStackSize</a>
</td>
<td align="left" width="63%">
Gets the size of the retrieval-filter stack in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C0709ECD-94CC-4745-A811-4180EC763CFC">GetStorageFilter</a>
</td>
<td align="left" width="63%">
Gets the storage filter at the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FE4D1749-7587-48BA-9701-B09DDFF1CE84">GetStorageFilterStackSize</a>
</td>
<td align="left" width="63%">
Gets the size of the storage-filter stack in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E766B599-1168-4E8C-9433-0200D34CD38D">PopRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pops a retrieval filter from the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B621336B-9334-4408-988F-6F5DBB2C4B53">PopStorageFilter</a>
</td>
<td align="left" width="63%">
Pops a storage filter from the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D1F82073-14DB-47B5-AB61-C1AFE5C50C42">PushCopyOfRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pushes a copy of the retrieval filter that is currently on the top of the retrieval-filter stack onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1CD32898-90B1-4523-8C97-985CA9F7D92B">PushCopyOfStorageFilter</a>
</td>
<td align="left" width="63%">
Pushes a copy of the storage filter that is currently on the top of the storage-filter stack onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/104C5BAD-D1FF-47EC-A1FA-C4B32EA4DFB6">PushDenyAllRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pushes a deny-all retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7985F43F-B0D3-4FF1-83D9-EEB568B29664">PushDenyAllStorageFilter</a>
</td>
<td align="left" width="63%">
Pushes a deny-all storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F6125FB9-EA1B-4052-A527-F4E5FAEE5C61">PushEmptyRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pushes an empty retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C0DC43B8-4869-49B0-A4D9-6907BCF1CB9E">PushEmptyStorageFilter</a>
</td>
<td align="left" width="63%">
Pushes an empty storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8027801C-ACDD-457D-A7A5-200B818D40A7">PushRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pushes a retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D90738A8-2C9F-4955-9A96-762C650F3B00">PushStorageFilter</a>
</td>
<td align="left" width="63%">
Pushes a storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/834C803B-EA7D-4D4C-B74E-9CF7914E0A4E">SetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Sets a message category to break on when a message with that category passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C225B262-B062-40D5-ADC0-491F47B111C9">SetBreakOnID</a>
</td>
<td align="left" width="63%">
Sets a message identifier to break on when a message with that identifier passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3316A9E5-F65B-4162-9A5E-CDB5CD65FBF8">SetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Sets a message severity level to break on when a message with that severity level passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77FFF3EA-DEBC-4D92-9C10-E382CD663D20">SetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Sets the maximum number of messages that can be added to the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F01E8BCC-CF82-4008-9829-C7EE4AD2973C">SetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Turns the debug output on or off.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by calling the <a href="https://msdn.microsoft.com/7702B842-6808-4CA9-A5B4-B1A1DC2479A7">DXGIGetDebugInterface</a> function.

For more info about the debug layer, see <a href="https://msdn.microsoft.com/c545983c-5351-42a9-82e5-deea73aa035f">Debug Layer</a>.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

