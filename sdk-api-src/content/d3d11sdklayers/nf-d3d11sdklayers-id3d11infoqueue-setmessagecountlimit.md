---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.SetMessageCountLimit
title: ID3D11InfoQueue::SetMessageCountLimit
author: windows-sdk-content
description: Set the maximum number of messages that can be added to the message queue.
old-location: direct3d11\id3d11infoqueue_setmessagecountlimit.htm
tech.root: direct3d11
ms.assetid: 59ed198c-65a5-4d78-867a-ba4527ad23c2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 56bf62b4-6ca7-b852-eada-d18cbf109706, ID3D11InfoQueue interface [Direct3D 11],SetMessageCountLimit method, ID3D11InfoQueue.SetMessageCountLimit, ID3D11InfoQueue::SetMessageCountLimit, SetMessageCountLimit, SetMessageCountLimit method [Direct3D 11], SetMessageCountLimit method [Direct3D 11],ID3D11InfoQueue interface, d3d11sdklayers/ID3D11InfoQueue::SetMessageCountLimit, direct3d11.id3d11infoqueue_setmessagecountlimit
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
 - ID3D11InfoQueue.SetMessageCountLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11InfoQueue::SetMessageCountLimit


## -description


Set the maximum number of messages that can be added to the message queue.


## -parameters




### -param MessageCountLimit [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT64</a></b>

Maximum number of messages that can be added to the message queue. -1 means no limit.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.




## -remarks



When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476538(v=VS.85).aspx">ID3D11InfoQueue Interface</a>
 

 

