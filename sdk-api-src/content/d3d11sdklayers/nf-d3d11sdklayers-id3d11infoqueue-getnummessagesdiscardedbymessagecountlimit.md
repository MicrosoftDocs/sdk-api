---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetNumMessagesDiscardedByMessageCountLimit
title: ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit
author: windows-sdk-content
description: Get the number of messages that were discarded due to the message count limit.
old-location: direct3d11\id3d11infoqueue_getnummessagesdiscardedbymessagecountlimit.htm
tech.root: direct3d11
ms.assetid: 8a2cb3c3-2b8c-47bf-b306-e13f35729686
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetNumMessagesDiscardedByMessageCountLimit, GetNumMessagesDiscardedByMessageCountLimit method [Direct3D 11], GetNumMessagesDiscardedByMessageCountLimit method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetNumMessagesDiscardedByMessageCountLimit method, ID3D11InfoQueue.GetNumMessagesDiscardedByMessageCountLimit, ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit, d3d11sdklayers/ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit, direct3d11.id3d11infoqueue_getnummessagesdiscardedbymessagecountlimit, ef744f2d-3777-9d02-76c3-9279cdf0497b
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
 - ID3D11InfoQueue.GetNumMessagesDiscardedByMessageCountLimit
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
- ID3D11InfoQueue.GetNumMessagesDiscardedByMessageCountLimit
: 
---

# ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit


## -description


Get the number of messages that were discarded due to the message count limit.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Number of messages discarded.




## -remarks



Get and set the message count limit with <a href="https://msdn.microsoft.com/971f3158-838d-4f1c-8d3c-15dac0b6dea9">ID3D11InfoQueue::GetMessageCountLimit</a> and <a href="https://msdn.microsoft.com/59ed198c-65a5-4d78-867a-ba4527ad23c2">ID3D11InfoQueue::SetMessageCountLimit</a>, respectively.




## -see-also




<a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>
 

 

