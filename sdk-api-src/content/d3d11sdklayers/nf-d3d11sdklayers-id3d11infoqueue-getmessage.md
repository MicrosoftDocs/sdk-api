---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetMessage
title: ID3D11InfoQueue::GetMessage
author: windows-sdk-content
description: Get a message from the message queue.
old-location: direct3d11\id3d11infoqueue_getmessage.htm
tech.root: direct3d11
ms.assetid: 685cddc5-cedd-410f-a693-665d2d69402e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetMessage, GetMessage method [Direct3D 11], GetMessage method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetMessage method, ID3D11InfoQueue.GetMessage, ID3D11InfoQueue::GetMessage, d3d11sdklayers/ID3D11InfoQueue::GetMessage, direct3d11.id3d11infoqueue_getmessage, fcb657d8-1742-cfff-a8cc-5af0bec46085
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11sdklayers.h
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
 - ID3D11InfoQueue.GetMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11sdklayers.h
: 
- ID3D11InfoQueue.GetMessage
: 
---

# ID3D11InfoQueue::GetMessage


## -description


Get a message from the message queue.


## -parameters




### -param MessageIndex [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT64</a></b>

Index into message queue after an optional retrieval filter has been applied. This can be between 0 and the number of messages in the message queue that pass through the retrieval filter (which can be obtained with <a href="https://msdn.microsoft.com/en-us/library/Ff476557(v=VS.85).aspx">ID3D11InfoQueue::GetNumStoredMessagesAllowedByRetrievalFilter</a>). 0 is the message at the front of the message queue.


### -param pMessage [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476184(v=VS.85).aspx">D3D11_MESSAGE</a>*</b>

Returned message (see <a href="https://msdn.microsoft.com/en-us/library/Ff476184(v=VS.85).aspx">D3D11_MESSAGE</a>).


### -param pMessageByteLength [in, out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">SIZE_T</a>*</b>

Size of pMessage in bytes, including the size of the message string that the pMessage points to.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.




## -remarks



This method does not remove any messages from the message queue.

This method gets messages from the message queue after an optional retrieval filter has been applied.

Applications should call this method twice to retrieve a message - first to obtain the size of the message and second to get the message. Here is a typical example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
// Get the size of the message
SIZE_T messageLength = 0;
HRESULT hr = pInfoQueue-&gt;GetMessage(0, NULL, &amp;messageLength);

// Allocate space and get the message
D3D11_MESSAGE * pMessage = (D3D11_MESSAGE*)malloc(messageLength);
hr = pInfoQueue-&gt;GetMessage(0, pMessage, &amp;messageLength);
</pre>
</td>
</tr>
</table></span></div>
For an overview see <a href="https://msdn.microsoft.com/en-us/library/Ff476538(v=VS.85).aspx">Information Queue Overview</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476538(v=VS.85).aspx">ID3D11InfoQueue Interface</a>
 

 

