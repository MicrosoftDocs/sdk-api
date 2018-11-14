---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetMessageCountLimit
title: ID3D10InfoQueue::GetMessageCountLimit
author: windows-sdk-content
description: Get the maximum number of messages that can be added to the message queue.
old-location: direct3d10\id3d10infoqueue_getmessagecountlimit.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getmessagecountlimit.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMessageCountLimit, GetMessageCountLimit method [Direct3D 10], GetMessageCountLimit method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],GetMessageCountLimit method, ID3D10InfoQueue.GetMessageCountLimit, ID3D10InfoQueue::GetMessageCountLimit, bf741d73-e29b-2506-211e-4de8244d540a, d3d10sdklayers/ID3D10InfoQueue::GetMessageCountLimit, direct3d10.id3d10infoqueue_getmessagecountlimit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.GetMessageCountLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10sdklayers.h
: 
- ID3D10InfoQueue.GetMessageCountLimit
: 
---

# ID3D10InfoQueue::GetMessageCountLimit


## -description


Get the maximum number of messages that can be added to the message queue.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Maximum number of messages that can be added to the queue. -1 means no limit.




## -remarks



When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173779(v=VS.85).aspx">ID3D10InfoQueue Interface</a>
 

 

