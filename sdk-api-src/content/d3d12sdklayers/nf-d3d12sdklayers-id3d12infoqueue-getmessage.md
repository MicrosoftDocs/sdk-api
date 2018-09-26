---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetMessage
title: ID3D12InfoQueue::GetMessage
author: windows-sdk-content
description: Get a message from the message queue.
old-location: direct3d12\id3d12infoqueue_getmessage.htm
tech.root: direct3d12
ms.assetid: B7B6D1C4-18FD-492A-8346-CA02FCD3EC4B
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetMessage, GetMessage method, GetMessage method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetMessage method, ID3D12InfoQueue.GetMessage, ID3D12InfoQueue::GetMessage, d3d12sdklayers/ID3D12InfoQueue::GetMessage, direct3d12.id3d12infoqueue_getmessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID3D12InfoQueue.GetMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12InfoQueue::GetMessage


## -description


Get a message from the message queue.




## -parameters




### -param MessageIndex [in]

Type: <b>UINT64</b>

Index into message queue after an optional retrieval filter has been applied. This can be between 0 and the number of messages in the message queue that pass through the retrieval filter (which can be obtained with <a href="https://msdn.microsoft.com/57F10336-2304-4DC9-B62B-6536A7AD76CB">GetNumStoredMessagesAllowedByRetrievalFilter</a>). 0 is the message at the front of the message queue.


          


### -param pMessage [out, optional]

Type: <b><a href="https://msdn.microsoft.com/DED84AC1-0126-450E-8A0A-1336BB4084D4">D3D12_MESSAGE</a>*</b>

Returned message.


### -param pMessageByteLength [in, out]

Type: <b>SIZE_T*</b>

Size of <i>pMessage</i> in bytes.




## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>. 
          




## -remarks



This method does not remove any messages from the message queue.



This method gets messages from the message queue after an optional retrieval filter has been applied.



Applications should call this method twice to retrieve a message - first to obtain the size of the message and second to get the message. Here is a typical example:



<pre class="syntax" xml:space="preserve"><code> 
// Get the size of the message
SIZE_T messageLength = 0;
HRESULT hr = pInfoQueue-&gt;GetMessage(0, NULL, &amp;messageLength);

// Allocate space and get the message
D3D12_MESSAGE * pMessage = (D3D12_MESSAGE*)malloc(messageLength);
hr = pInfoQueue-&gt;GetMessage(0, pMessage, &amp;messageLength); 
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a>
 

 

