---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.AddMessage
title: ID3D11InfoQueue::AddMessage method
author: windows-driver-content
description: Add a debug message to the message queue and send that message to debug output.
old-location: direct3d11\id3d11infoqueue_addmessage.htm
old-project: direct3d11
ms.assetid: 7265a273-327a-482b-9d47-6931e031cff8
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 1ac22c4e-5bd3-bec5-0c6b-508a2b311005, AddMessage method [Direct3D 11], AddMessage method [Direct3D 11], ID3D11InfoQueue interface, AddMessage,ID3D11InfoQueue.AddMessage, ID3D11InfoQueue, ID3D11InfoQueue interface [Direct3D 11], AddMessage method, ID3D11InfoQueue::AddMessage, d3d11sdklayers/ID3D11InfoQueue::AddMessage, direct3d11.id3d11infoqueue_addmessage
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
-	ID3D11InfoQueue.AddMessage
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11InfoQueue::AddMessage method


## -description


Add a debug message to the message queue and send that message to debug output.


## -parameters




### -param Category [in]

Type: <b><a href="https://msdn.microsoft.com/e4af5bf6-cbbe-488a-ad8e-3a4409f2591d">D3D11_MESSAGE_CATEGORY</a></b>

Category of a message (see <a href="https://msdn.microsoft.com/e4af5bf6-cbbe-488a-ad8e-3a4409f2591d">D3D11_MESSAGE_CATEGORY</a>).


### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/63143187-8e16-4ba4-aec5-8530ed31accb">D3D11_MESSAGE_SEVERITY</a></b>

Severity of a message (see <a href="https://msdn.microsoft.com/63143187-8e16-4ba4-aec5-8530ed31accb">D3D11_MESSAGE_SEVERITY</a>).


### -param ID [in]

Type: <b><a href="https://msdn.microsoft.com/50dde92d-9856-4010-8848-485a8d92b145">D3D11_MESSAGE_ID</a></b>

Unique identifier of a message (see <a href="https://msdn.microsoft.com/50dde92d-9856-4010-8848-485a8d92b145">D3D11_MESSAGE_ID</a>).


### -param pDescription [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

User-defined message.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



This method is used by the runtime's internal mechanisms to add debug messages to the message queue and send them to debug output. For applications to add their own custom messages to the message queue and send them to debug output, call <a href="https://msdn.microsoft.com/ca5a5e33-f912-4283-8b23-b212ace6089c">ID3D11InfoQueue::AddApplicationMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>
 

 

