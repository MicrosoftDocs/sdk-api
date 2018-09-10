---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.AddMessage
title: ID3D10InfoQueue::AddMessage
author: windows-sdk-content
description: Add a Direct3D 10 debug message to the message queue and send that message to debug output.
old-location: direct3d10\id3d10infoqueue_addmessage.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_addmessage.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: AddMessage, AddMessage method [Direct3D 10], AddMessage method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],AddMessage method, ID3D10InfoQueue.AddMessage, ID3D10InfoQueue::AddMessage, cdfe0171-65a2-02d0-bad5-e630bf30db83, d3d10sdklayers/ID3D10InfoQueue::AddMessage, direct3d10.id3d10infoqueue_addmessage
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
 - ID3D10InfoQueue.AddMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10InfoQueue::AddMessage


## -description


Add a Direct3D 10 debug message to the message queue and send that message to debug output.


## -parameters




### -param Category [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205323(v=VS.85).aspx">D3D10_MESSAGE_CATEGORY</a></b>

Category of a message (see <a href="https://msdn.microsoft.com/en-us/library/Bb205323(v=VS.85).aspx">D3D10_MESSAGE_CATEGORY</a>).


### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205325(v=VS.85).aspx">D3D10_MESSAGE_SEVERITY</a></b>

Severity of a message (see <a href="https://msdn.microsoft.com/en-us/library/Bb205325(v=VS.85).aspx">D3D10_MESSAGE_SEVERITY</a>).


### -param ID [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205324(v=VS.85).aspx">D3D10_MESSAGE_ID</a></b>

Unique identifier of a message (see <a href="https://msdn.microsoft.com/en-us/library/Bb205324(v=VS.85).aspx">D3D10_MESSAGE_ID</a>).


### -param pDescription [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

User-defined message.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



This method is used by the runtime's internal mechanisms to add Direct3D 10 debug messages to the message queue and send them to debug output. For applications to add their own custom messages to the message queue and send them to debug output, call <a href="https://msdn.microsoft.com/en-us/library/Bb173780(v=VS.85).aspx">ID3D10InfoQueue::AddApplicationMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173779(v=VS.85).aspx">ID3D10InfoQueue Interface</a>
 

 

