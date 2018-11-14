---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.AddApplicationMessage
title: ID3D10InfoQueue::AddApplicationMessage
author: windows-sdk-content
description: Add a user-defined message to the message queue and send that message to debug output.
old-location: direct3d10\id3d10infoqueue_addapplicationmessage.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_addapplicationmessage.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 1d152bbb-d6ef-f0f3-d61f-2156408503ce, AddApplicationMessage, AddApplicationMessage method [Direct3D 10], AddApplicationMessage method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],AddApplicationMessage method, ID3D10InfoQueue.AddApplicationMessage, ID3D10InfoQueue::AddApplicationMessage, d3d10sdklayers/ID3D10InfoQueue::AddApplicationMessage, direct3d10.id3d10infoqueue_addapplicationmessage
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
 - ID3D10InfoQueue.AddApplicationMessage
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
- ID3D10InfoQueue.AddApplicationMessage
: 
---

# ID3D10InfoQueue::AddApplicationMessage


## -description


Add a user-defined message to the message queue and send that message to debug output.


## -parameters




### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/548487cb-1315-45b2-86df-f32d129a1212">D3D10_MESSAGE_SEVERITY</a></b>

Severity of a message (see <a href="https://msdn.microsoft.com/548487cb-1315-45b2-86df-f32d129a1212">D3D10_MESSAGE_SEVERITY</a>).


### -param pDescription [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Message string.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>
 

 

