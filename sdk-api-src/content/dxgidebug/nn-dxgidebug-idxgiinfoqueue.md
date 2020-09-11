---
UID: NN:dxgidebug.IDXGIInfoQueue
title: IDXGIInfoQueue (dxgidebug.h)
description: This interface controls the debug information queue, and can only be used if the debug layer is turned on.
helpviewer_keywords: ["IDXGIInfoQueue","IDXGIInfoQueue interface [DXGI]","IDXGIInfoQueue interface [DXGI]","described","direct3ddxgi.idxgiinfoqueue","dxgidebug/IDXGIInfoQueue"]
old-location: direct3ddxgi\idxgiinfoqueue.htm
tech.root: direct3ddxgi
ms.assetid: F1BC6752-F334-4E8C-BE42-B731635A799D
ms.date: 12/05/2018
ms.keywords: IDXGIInfoQueue, IDXGIInfoQueue interface [DXGI], IDXGIInfoQueue interface [DXGI],described, direct3ddxgi.idxgiinfoqueue, dxgidebug/IDXGIInfoQueue
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: DXGIDebug.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIInfoQueue
 - dxgidebug/IDXGIInfoQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIInfoQueue
---

# IDXGIInfoQueue interface


## -description

This interface controls the debug information queue, and can only be used if the debug layer is turned on.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIInfoQueue</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDXGIInfoQueue</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-addapplicationmessage">AddApplicationMessage</a>
</td>
<td align="left" width="63%">
Adds a user-defined message to the message queue and sends that message to the debug output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-addmessage">AddMessage</a>
</td>
<td align="left" width="63%">
Adds a debug message to the message queue and sends that message to the debug output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-addretrievalfilterentries">AddRetrievalFilterEntries</a>
</td>
<td align="left" width="63%">
Adds retrieval filters to the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-addstoragefilterentries">AddStorageFilterEntries</a>
</td>
<td align="left" width="63%">
Adds storage filters to the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-clearretrievalfilter">ClearRetrievalFilter</a>
</td>
<td align="left" width="63%">
Removes a retrieval filter from the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-clearstoragefilter">ClearStorageFilter</a>
</td>
<td align="left" width="63%">
Removes a storage filter from the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-clearstoredmessages">ClearStoredMessages</a>
</td>
<td align="left" width="63%">
Clears all messages from the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getbreakoncategory">GetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Determines whether the break on a message category is turned on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getbreakonid">GetBreakOnID</a>
</td>
<td align="left" width="63%">
Determines whether the break on a message identifier is turned on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getbreakonseverity">GetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Determines whether the break on a message severity level is turned on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getmessage">GetMessage</a>
</td>
<td align="left" width="63%">
Gets a message from the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getmessagecountlimit">GetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Gets the maximum number of messages that can be added to the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getmutedebugoutput">GetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Determines whether the debug output is turned on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getnummessagesallowedbystoragefilter">GetNumMessagesAllowedByStorageFilter</a>
</td>
<td align="left" width="63%">
Gets the number of messages that a storage filter allowed to pass through.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getnummessagesdeniedbystoragefilter">GetNumMessagesDeniedByStorageFilter</a>
</td>
<td align="left" width="63%">
Gets the number of messages that were denied passage through a storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getnummessagesdiscardedbymessagecountlimit">GetNumMessagesDiscardedByMessageCountLimit</a>
</td>
<td align="left" width="63%">
Gets the number of messages that were discarded due to the message count limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getnumstoredmessages">GetNumStoredMessages</a>
</td>
<td align="left" width="63%">
Gets the number of messages currently stored in the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getnumstoredmessagesallowedbyretrievalfilters">GetNumStoredMessagesAllowedByRetrievalFilters</a>
</td>
<td align="left" width="63%">
Gets the number of messages that can pass through a retrieval filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getretrievalfilter">GetRetrievalFilter</a>
</td>
<td align="left" width="63%">
Gets the retrieval filter at the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getretrievalfilterstacksize">GetRetrievalFilterStackSize</a>
</td>
<td align="left" width="63%">
Gets the size of the retrieval-filter stack in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getstoragefilter">GetStorageFilter</a>
</td>
<td align="left" width="63%">
Gets the storage filter at the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getstoragefilterstacksize">GetStorageFilterStackSize</a>
</td>
<td align="left" width="63%">
Gets the size of the storage-filter stack in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-popretrievalfilter">PopRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pops a retrieval filter from the top of the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-popstoragefilter">PopStorageFilter</a>
</td>
<td align="left" width="63%">
Pops a storage filter from the top of the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-pushcopyofretrievalfilter">PushCopyOfRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pushes a copy of the retrieval filter that is currently on the top of the retrieval-filter stack onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-pushcopyofstoragefilter">PushCopyOfStorageFilter</a>
</td>
<td align="left" width="63%">
Pushes a copy of the storage filter that is currently on the top of the storage-filter stack onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-pushdenyallretrievalfilter">PushDenyAllRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pushes a deny-all retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-pushdenyallstoragefilter">PushDenyAllStorageFilter</a>
</td>
<td align="left" width="63%">
Pushes a deny-all storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-pushemptyretrievalfilter">PushEmptyRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pushes an empty retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-pushemptystoragefilter">PushEmptyStorageFilter</a>
</td>
<td align="left" width="63%">
Pushes an empty storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-pushretrievalfilter">PushRetrievalFilter</a>
</td>
<td align="left" width="63%">
Pushes a retrieval filter onto the retrieval-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-pushstoragefilter">PushStorageFilter</a>
</td>
<td align="left" width="63%">
Pushes a storage filter onto the storage-filter stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-setbreakoncategory">SetBreakOnCategory</a>
</td>
<td align="left" width="63%">
Sets a message category to break on when a message with that category passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-setbreakonid">SetBreakOnID</a>
</td>
<td align="left" width="63%">
Sets a message identifier to break on when a message with that identifier passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-setbreakonseverity">SetBreakOnSeverity</a>
</td>
<td align="left" width="63%">
Sets a message severity level to break on when a message with that severity level passes through the storage filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-setmessagecountlimit">SetMessageCountLimit</a>
</td>
<td align="left" width="63%">
Sets the maximum number of messages that can be added to the message queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-setmutedebugoutput">SetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Turns the debug output on or off.

</td>
</tr>
</table>

## -remarks

This interface is obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/dxgidebug/nf-dxgidebug-dxgigetdebuginterface">DXGIGetDebugInterface</a> function.

For more info about the debug layer, see <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">Debug Layer</a>.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

