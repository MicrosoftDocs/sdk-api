---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.SetMessageCountLimit
title: ID3D10InfoQueue::SetMessageCountLimit
author: windows-sdk-content
description: Set the maximum number of messages that can be added to the message queue.
old-location: direct3d10\id3d10infoqueue_setmessagecountlimit.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_setmessagecountlimit.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 27e01700-9801-1813-918b-c6687b02eb6f, ID3D10InfoQueue interface [Direct3D 10],SetMessageCountLimit method, ID3D10InfoQueue.SetMessageCountLimit, ID3D10InfoQueue::SetMessageCountLimit, SetMessageCountLimit, SetMessageCountLimit method [Direct3D 10], SetMessageCountLimit method [Direct3D 10],ID3D10InfoQueue interface, d3d10sdklayers/ID3D10InfoQueue::SetMessageCountLimit, direct3d10.id3d10infoqueue_setmessagecountlimit
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
 - ID3D10InfoQueue.SetMessageCountLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10InfoQueue::SetMessageCountLimit


## -description


Set the maximum number of messages that can be added to the message queue.


## -parameters




### -param MessageCountLimit [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Maximum number of messages that can be added to the message queue. -1 means no limit.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.




## -see-also




<a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>
 

 

