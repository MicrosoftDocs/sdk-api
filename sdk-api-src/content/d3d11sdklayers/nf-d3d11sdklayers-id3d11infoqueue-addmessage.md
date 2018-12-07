---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.AddMessage
title: ID3D11InfoQueue::AddMessage
author: windows-sdk-content
description: Add a debug message to the message queue and send that message to debug output.
old-location: direct3d11\id3d11infoqueue_addmessage.htm
tech.root: direct3d11
ms.assetid: 7265a273-327a-482b-9d47-6931e031cff8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 1ac22c4e-5bd3-bec5-0c6b-508a2b311005, AddMessage, AddMessage method [Direct3D 11], AddMessage method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],AddMessage method, ID3D11InfoQueue.AddMessage, ID3D11InfoQueue::AddMessage, d3d11sdklayers/ID3D11InfoQueue::AddMessage, direct3d11.id3d11infoqueue_addmessage
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
 - ID3D11InfoQueue.AddMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11InfoQueue::AddMessage


## -description


Add a debug message to the message queue and send that message to debug output.


## -parameters




### -param Category [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476185(v=VS.85).aspx">D3D11_MESSAGE_CATEGORY</a></b>

Category of a message (see <a href="https://msdn.microsoft.com/en-us/library/Ff476185(v=VS.85).aspx">D3D11_MESSAGE_CATEGORY</a>).


### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476187(v=VS.85).aspx">D3D11_MESSAGE_SEVERITY</a></b>

Severity of a message (see <a href="https://msdn.microsoft.com/en-us/library/Ff476187(v=VS.85).aspx">D3D11_MESSAGE_SEVERITY</a>).


### -param ID [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476186(v=VS.85).aspx">D3D11_MESSAGE_ID</a></b>

Unique identifier of a message (see <a href="https://msdn.microsoft.com/en-us/library/Ff476186(v=VS.85).aspx">D3D11_MESSAGE_ID</a>).


### -param pDescription [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCSTR</a></b>

User-defined message.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.




## -remarks



This method is used by the runtime's internal mechanisms to add debug messages to the message queue and send them to debug output. For applications to add their own custom messages to the message queue and send them to debug output, call <a href="https://msdn.microsoft.com/en-us/library/Ff476539(v=VS.85).aspx">ID3D11InfoQueue::AddApplicationMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476538(v=VS.85).aspx">ID3D11InfoQueue Interface</a>
 

 

