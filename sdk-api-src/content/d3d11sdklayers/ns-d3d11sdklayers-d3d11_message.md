---
UID: NS:d3d11sdklayers.D3D11_MESSAGE
title: D3D11_MESSAGE
author: windows-sdk-content
description: A debug message in the Information Queue.
old-location: direct3d11\d3d11_message.htm
tech.root: direct3d11
ms.assetid: b00a7e61-5394-40bd-bdc1-94da45dfa264
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 63ec230f-4005-c7e9-9187-f8c6f44e0780, D3D11_MESSAGE, D3D11_MESSAGE structure [Direct3D 11], d3d11sdklayers/D3D11_MESSAGE, direct3d11.d3d11_message
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11SDKLayers.h
api_name:
 - D3D11_MESSAGE
product: Windows
targetos: Windows
req.typenames: D3D11_MESSAGE
req.redist: 
---

# D3D11_MESSAGE structure


## -description


A debug message in the Information Queue.


## -struct-fields




### -field Category

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476185(v=VS.85).aspx">D3D11_MESSAGE_CATEGORY</a></b>

The category of the message. See <a href="https://msdn.microsoft.com/en-us/library/Ff476185(v=VS.85).aspx">D3D11_MESSAGE_CATEGORY</a>.


### -field Severity

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476187(v=VS.85).aspx">D3D11_MESSAGE_SEVERITY</a></b>

The severity of the message. See <a href="https://msdn.microsoft.com/en-us/library/Ff476187(v=VS.85).aspx">D3D11_MESSAGE_SEVERITY</a>.


### -field ID

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476186(v=VS.85).aspx">D3D11_MESSAGE_ID</a></b>

The ID of the message. See <a href="https://msdn.microsoft.com/en-us/library/Ff476186(v=VS.85).aspx">D3D11_MESSAGE_ID</a>.


### -field pDescription

Type: <b>const char*</b>

The message string.


### -field DescriptionByteLength

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">SIZE_T</a></b>

The length of pDescription in bytes.


## -remarks



This structure is returned from <a href="https://msdn.microsoft.com/en-us/library/Ff476549(v=VS.85).aspx">ID3D11InfoQueue::GetMessage</a> as part of the Information Queue feature (see <a href="https://msdn.microsoft.com/en-us/library/Ff476538(v=VS.85).aspx">ID3D11InfoQueue Interface</a>).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476159(v=VS.85).aspx">Layer Structures</a>
 

 

