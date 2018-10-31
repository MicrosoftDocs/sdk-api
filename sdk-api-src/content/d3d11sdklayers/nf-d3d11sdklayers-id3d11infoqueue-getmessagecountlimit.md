---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetMessageCountLimit
title: ID3D11InfoQueue::GetMessageCountLimit
author: windows-sdk-content
description: Get the maximum number of messages that can be added to the message queue.
old-location: direct3d11\id3d11infoqueue_getmessagecountlimit.htm
tech.root: direct3d11
ms.assetid: 971f3158-838d-4f1c-8d3c-15dac0b6dea9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMessageCountLimit, GetMessageCountLimit method [Direct3D 11], GetMessageCountLimit method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetMessageCountLimit method, ID3D11InfoQueue.GetMessageCountLimit, ID3D11InfoQueue::GetMessageCountLimit, d3d11sdklayers/ID3D11InfoQueue::GetMessageCountLimit, direct3d11.id3d11infoqueue_getmessagecountlimit, f8f0d99b-4472-147b-2074-368f1ee90957
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
 - ID3D11InfoQueue.GetMessageCountLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11InfoQueue::GetMessageCountLimit


## -description


Get the maximum number of messages that can be added to the message queue.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Maximum number of messages that can be added to the queue. -1 means no limit.




## -remarks



When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.




## -see-also




<a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>
 

 

