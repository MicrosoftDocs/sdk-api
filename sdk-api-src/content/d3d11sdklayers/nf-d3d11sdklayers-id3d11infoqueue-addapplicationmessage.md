---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.AddApplicationMessage
title: ID3D11InfoQueue::AddApplicationMessage
author: windows-sdk-content
description: Add a user-defined message to the message queue and send that message to debug output.
old-location: direct3d11\id3d11infoqueue_addapplicationmessage.htm
tech.root: direct3d11
ms.assetid: ca5a5e33-f912-4283-8b23-b212ace6089c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 566d6299-a5dc-568a-e71a-3c990b282e93, AddApplicationMessage, AddApplicationMessage method [Direct3D 11], AddApplicationMessage method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],AddApplicationMessage method, ID3D11InfoQueue.AddApplicationMessage, ID3D11InfoQueue::AddApplicationMessage, d3d11sdklayers/ID3D11InfoQueue::AddApplicationMessage, direct3d11.id3d11infoqueue_addapplicationmessage
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
 - ID3D11InfoQueue.AddApplicationMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11InfoQueue::AddApplicationMessage


## -description


Add a user-defined message to the message queue and send that message to debug output.


## -parameters




### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476187(v=VS.85).aspx">D3D11_MESSAGE_SEVERITY</a></b>

Severity of a message (see <a href="https://msdn.microsoft.com/en-us/library/Ff476187(v=VS.85).aspx">D3D11_MESSAGE_SEVERITY</a>).


### -param pDescription [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCSTR</a></b>

Message string.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476538(v=VS.85).aspx">ID3D11InfoQueue Interface</a>
 

 

