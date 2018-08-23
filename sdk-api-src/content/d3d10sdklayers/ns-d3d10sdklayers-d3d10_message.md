---
UID: NS:d3d10sdklayers.D3D10_MESSAGE
title: D3D10_MESSAGE
author: windows-sdk-content
description: A debug message in the Information Queue.
old-location: direct3d10\d3d10_message.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_message.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 3d6907d3-259d-0e6a-db64-2a00690f975d, D3D10_MESSAGE, D3D10_MESSAGE structure [Direct3D 10], d3d10sdklayers/D3D10_MESSAGE, direct3d10.d3d10_message
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10sdklayers.h
req.include-header: D3D10.h
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
req.typenames: D3D10_MESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10sdklayers.h
api_name:
 - D3D10_MESSAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_MESSAGE structure


## -description


A debug message in the Information Queue.


## -struct-fields




### -field Category

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205323(v=VS.85).aspx">D3D10_MESSAGE_CATEGORY</a></b>

The category of the message. See <a href="https://msdn.microsoft.com/en-us/library/Bb205323(v=VS.85).aspx">D3D10_MESSAGE_CATEGORY</a>.


### -field Severity

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205325(v=VS.85).aspx">D3D10_MESSAGE_SEVERITY</a></b>

The severity of the message. See <a href="https://msdn.microsoft.com/en-us/library/Bb205325(v=VS.85).aspx">D3D10_MESSAGE_SEVERITY</a>.


### -field ID

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205324(v=VS.85).aspx">D3D10_MESSAGE_ID</a></b>

The ID of the message. See <a href="https://msdn.microsoft.com/en-us/library/Bb205324(v=VS.85).aspx">D3D10_MESSAGE_ID</a>.


### -field pDescription

Type: <b>const char*</b>

The message string.


### -field DescriptionByteLength

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

The length of pDescription in bytes.


## -remarks



This structure is returned from <a href="https://msdn.microsoft.com/en-us/library/Bb173790(v=VS.85).aspx">ID3D10InfoQueue::GetMessage</a> as part of the Information Queue feature (see <a href="https://msdn.microsoft.com/en-us/library/Bb173779(v=VS.85).aspx">ID3D10InfoQueue Interface</a>).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205153(v=VS.85).aspx">Core Structures</a>
 

 

