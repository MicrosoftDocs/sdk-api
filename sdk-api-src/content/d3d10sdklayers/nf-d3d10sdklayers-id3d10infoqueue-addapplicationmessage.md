---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.AddApplicationMessage
title: ID3D10InfoQueue::AddApplicationMessage
author: windows-sdk-content
description: Add a user-defined message to the message queue and send that message to debug output.
old-location: direct3d10\id3d10infoqueue_addapplicationmessage.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_addapplicationmessage.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 1d152bbb-d6ef-f0f3-d61f-2156408503ce, AddApplicationMessage, AddApplicationMessage method [Direct3D 10], AddApplicationMessage method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],AddApplicationMessage method, ID3D10InfoQueue.AddApplicationMessage, ID3D10InfoQueue::AddApplicationMessage, d3d10sdklayers/ID3D10InfoQueue::AddApplicationMessage, direct3d10.id3d10infoqueue_addapplicationmessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10sdklayers.h
req.include-header: 
req.redist: 
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
 - ID3D10InfoQueue.AddApplicationMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10InfoQueue::AddApplicationMessage


## -description


Add a user-defined message to the message queue and send that message to debug output.


## -parameters




### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205325(v=VS.85).aspx">D3D10_MESSAGE_SEVERITY</a></b>

Severity of a message (see <a href="https://msdn.microsoft.com/en-us/library/Bb205325(v=VS.85).aspx">D3D10_MESSAGE_SEVERITY</a>).


### -param pDescription [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Message string.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173779(v=VS.85).aspx">ID3D10InfoQueue Interface</a>
 

 

