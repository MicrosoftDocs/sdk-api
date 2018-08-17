---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.AddMessage
title: ID3D10InfoQueue::AddMessage
author: windows-sdk-content
description: Add a Direct3D 10 debug message to the message queue and send that message to debug output.
old-location: direct3d10\id3d10infoqueue_addmessage.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_addmessage.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AddMessage, AddMessage method [Direct3D 10], AddMessage method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],AddMessage method, ID3D10InfoQueue.AddMessage, ID3D10InfoQueue::AddMessage, cdfe0171-65a2-02d0-bad5-e630bf30db83, d3d10sdklayers/ID3D10InfoQueue::AddMessage, direct3d10.id3d10infoqueue_addmessage
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
 - ID3D10InfoQueue.AddMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10InfoQueue::AddMessage


## -description


Add a Direct3D 10 debug message to the message queue and send that message to debug output.


## -parameters




### -param Category [in]

Type: <b><a href="https://msdn.microsoft.com/35256b90-4ba4-45ec-ad3e-a19884868740">D3D10_MESSAGE_CATEGORY</a></b>

Category of a message (see <a href="https://msdn.microsoft.com/35256b90-4ba4-45ec-ad3e-a19884868740">D3D10_MESSAGE_CATEGORY</a>).


### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/548487cb-1315-45b2-86df-f32d129a1212">D3D10_MESSAGE_SEVERITY</a></b>

Severity of a message (see <a href="https://msdn.microsoft.com/548487cb-1315-45b2-86df-f32d129a1212">D3D10_MESSAGE_SEVERITY</a>).


### -param ID [in]

Type: <b><a href="https://msdn.microsoft.com/c5c07158-d102-4064-94e7-eecf8b60ac98">D3D10_MESSAGE_ID</a></b>

Unique identifier of a message (see <a href="https://msdn.microsoft.com/c5c07158-d102-4064-94e7-eecf8b60ac98">D3D10_MESSAGE_ID</a>).


### -param pDescription [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

User-defined message.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



This method is used by the runtime's internal mechanisms to add Direct3D 10 debug messages to the message queue and send them to debug output. For applications to add their own custom messages to the message queue and send them to debug output, call <a href="https://msdn.microsoft.com/223f9a01-4507-4877-bd86-c5b9cb441d7a">ID3D10InfoQueue::AddApplicationMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>
 

 

