---
UID: NF:dxgidebug.IDXGIInfoQueue.GetMessage
title: IDXGIInfoQueue::GetMessage
author: windows-sdk-content
description: Gets a message from the message queue.
old-location: direct3ddxgi\idxgiinfoqueue_getmessage.htm
old-project: direct3ddxgi
ms.assetid: 208C3253-09AE-4379-808D-BA0BECC59BF8
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetMessage, GetMessage method [DXGI], GetMessage method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetMessage method, IDXGIInfoQueue.GetMessage, IDXGIInfoQueue::GetMessage, direct3ddxgi.idxgiinfoqueue_getmessage, dxgidebug/IDXGIInfoQueue::GetMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IDXGIInfoQueue.GetMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIInfoQueue::GetMessage


## -description


Gets a message from the message queue.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that gets the message.


### -param MessageIndex [in]

An index into the message queue after an optional retrieval filter has been applied. This can be between 0 and the number of messages in the message queue that pass through the retrieval filter. Call <a href="https://msdn.microsoft.com/1BFFEE9F-7902-41B7-9607-BD0E955FBD8B">IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters</a> to obtain this number. 0 is the message at the beginning of the message queue.


### -param pMessage [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/F0FF1DC6-8E62-4D35-BCB7-EC3BB314F033">DXGI_INFO_QUEUE_MESSAGE</a> structure that describes the message.


### -param pMessageByteLength [in, out]

A pointer to a variable that receives the size, in bytes, of the message description  that <i>pMessage</i> points to. This size includes the size of the message string that <i>pMessage</i> points to.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



This method doesn't remove any messages from the message queue.

This method gets a message from the message queue after an optional retrieval filter has been applied.

Call this method twice to retrieve a message, first to obtain the size of the message and second to get the message. Here is a typical example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
// Get the size of the message.
SIZE_T messageLength = 0;
HRESULT hr = pInfoQueue-&gt;GetMessage(DXGI_DEBUG_ALL, 0, NULL, &amp;messageLength);

// Allocate space and get the message.
DXGI_INFO_QUEUE_MESSAGE * pMessage = (DXGI_INFO_QUEUE_MESSAGE*)malloc(messageLength);
hr = pInfoQueue-&gt;GetMessage(DXGI_DEBUG_ALL, 0, pMessage, &amp;messageLength);
</pre>
</td>
</tr>
</table></span></div>
<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

