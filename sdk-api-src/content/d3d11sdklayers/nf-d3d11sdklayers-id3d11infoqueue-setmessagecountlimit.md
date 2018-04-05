---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.SetMessageCountLimit
title: ID3D11InfoQueue::SetMessageCountLimit method
author: windows-driver-content
description: Set the maximum number of messages that can be added to the message queue.
old-location: direct3d11\id3d11infoqueue_setmessagecountlimit.htm
old-project: direct3d11
ms.assetid: 59ed198c-65a5-4d78-867a-ba4527ad23c2
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 56bf62b4-6ca7-b852-eada-d18cbf109706, ID3D11InfoQueue, ID3D11InfoQueue interface [Direct3D 11], SetMessageCountLimit method, ID3D11InfoQueue::SetMessageCountLimit, SetMessageCountLimit method [Direct3D 11], SetMessageCountLimit method [Direct3D 11], ID3D11InfoQueue interface, SetMessageCountLimit,ID3D11InfoQueue.SetMessageCountLimit, d3d11sdklayers/ID3D11InfoQueue::SetMessageCountLimit, direct3d11.id3d11infoqueue_setmessagecountlimit
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
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11InfoQueue.SetMessageCountLimit
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11InfoQueue::SetMessageCountLimit method


## -description


Set the maximum number of messages that can be added to the message queue.


## -parameters




### -param MessageCountLimit [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Maximum number of messages that can be added to the message queue. -1 means no limit.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.




## -see-also




<a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>
 

 

