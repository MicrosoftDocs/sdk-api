---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.SetMessageCountLimit
title: ID3D10InfoQueue::SetMessageCountLimit
author: windows-sdk-content
description: Set the maximum number of messages that can be added to the message queue.
old-location: direct3d10\id3d10infoqueue_setmessagecountlimit.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_setmessagecountlimit.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 27e01700-9801-1813-918b-c6687b02eb6f, ID3D10InfoQueue interface [Direct3D 10],SetMessageCountLimit method, ID3D10InfoQueue.SetMessageCountLimit, ID3D10InfoQueue::SetMessageCountLimit, SetMessageCountLimit, SetMessageCountLimit method [Direct3D 10], SetMessageCountLimit method [Direct3D 10],ID3D10InfoQueue interface, d3d10sdklayers/ID3D10InfoQueue::SetMessageCountLimit, direct3d10.id3d10infoqueue_setmessagecountlimit
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.SetMessageCountLimit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10InfoQueue::SetMessageCountLimit


## -description


Set the maximum number of messages that can be added to the message queue.


## -parameters




### -param MessageCountLimit [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Maximum number of messages that can be added to the message queue. -1 means no limit.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173779(v=VS.85).aspx">ID3D10InfoQueue Interface</a>
 

 

