---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.SetMessageCountLimit
title: ID3D12InfoQueue::SetMessageCountLimit
author: windows-sdk-content
description: Set the maximum number of messages that can be added to the message queue.
old-location: direct3d12\id3d12infoqueue_setmessagecountlimit.htm
tech.root: direct3d12
ms.assetid: A3C21C98-2B31-4901-8ED6-55E68507D200
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ID3D12InfoQueue interface,SetMessageCountLimit method, ID3D12InfoQueue.SetMessageCountLimit, ID3D12InfoQueue::SetMessageCountLimit, SetMessageCountLimit, SetMessageCountLimit method, SetMessageCountLimit method,ID3D12InfoQueue interface, d3d12sdklayers/ID3D12InfoQueue::SetMessageCountLimit, direct3d12.id3d12infoqueue_setmessagecountlimit
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
 - ID3D12InfoQueue.SetMessageCountLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12InfoQueue::SetMessageCountLimit


## -description


Set the maximum number of messages that can be added to the message queue.


        


## -parameters




### -param MessageCountLimit [in]

Type: <b>UINT64</b>

Maximum number of messages that can be added to the message queue. -1 means no limit.

When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.




## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>. 
          




## -see-also




<a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a>
 

 

