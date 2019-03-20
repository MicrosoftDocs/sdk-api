---
UID: NS:d3d11sdklayers.D3D11_MESSAGE
title: D3D11_MESSAGE (d3d11sdklayers.h)
author: windows-sdk-content
description: A debug message in the Information Queue.
old-location: direct3d11\d3d11_message.htm
tech.root: direct3d11
ms.assetid: b00a7e61-5394-40bd-bdc1-94da45dfa264
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 63ec230f-4005-c7e9-9187-f8c6f44e0780, D3D11_MESSAGE, D3D11_MESSAGE structure [Direct3D 11], d3d11sdklayers/D3D11_MESSAGE, direct3d11.d3d11_message
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

Type: <b><a href="https://msdn.microsoft.com/e4af5bf6-cbbe-488a-ad8e-3a4409f2591d">D3D11_MESSAGE_CATEGORY</a></b>

The category of the message. See <a href="https://msdn.microsoft.com/e4af5bf6-cbbe-488a-ad8e-3a4409f2591d">D3D11_MESSAGE_CATEGORY</a>.


### -field Severity

Type: <b><a href="https://msdn.microsoft.com/63143187-8e16-4ba4-aec5-8530ed31accb">D3D11_MESSAGE_SEVERITY</a></b>

The severity of the message. See <a href="https://msdn.microsoft.com/63143187-8e16-4ba4-aec5-8530ed31accb">D3D11_MESSAGE_SEVERITY</a>.


### -field ID

Type: <b><a href="https://msdn.microsoft.com/50dde92d-9856-4010-8848-485a8d92b145">D3D11_MESSAGE_ID</a></b>

The ID of the message. See <a href="https://msdn.microsoft.com/50dde92d-9856-4010-8848-485a8d92b145">D3D11_MESSAGE_ID</a>.


### -field pDescription

Type: <b>const char*</b>

The message string.


### -field DescriptionByteLength

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

The length of pDescription in bytes.


## -remarks



This structure is returned from <a href="https://msdn.microsoft.com/685cddc5-cedd-410f-a693-665d2d69402e">ID3D11InfoQueue::GetMessage</a> as part of the Information Queue feature (see <a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>).




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>



<a href="https://msdn.microsoft.com/65f0830f-f009-47fb-b04e-24790e677338">Layer Structures</a>
 

 

