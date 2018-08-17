---
UID: NS:d3d12sdklayers.D3D12_MESSAGE
title: D3D12_MESSAGE
author: windows-sdk-content
description: A debug message in the Information Queue.
old-location: direct3d12\d3d12_message.htm
old-project: direct3d12
ms.assetid: DED84AC1-0126-450E-8A0A-1336BB4084D4
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_MESSAGE, D3D12_MESSAGE structure, d3d12sdklayers/D3D12_MESSAGE, direct3d12.d3d12_message
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12sdklayers.h
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
req.typenames: D3D12_MESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12sdklayers.h
api_name:
 - D3D12_MESSAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_MESSAGE structure


## -description


A debug message in the Information Queue.


## -struct-fields




### -field Category

The category of the message. See <a href="https://msdn.microsoft.com/en-us/library/Dn950145(v=VS.85).aspx">D3D12_MESSAGE_CATEGORY</a>.
          


### -field Severity

The severity of the message. See  <a href="https://msdn.microsoft.com/en-us/library/Dn950147(v=VS.85).aspx">D3D12_MESSAGE_SEVERITY</a>.
          


### -field ID

The ID of the message. See <a href="https://msdn.microsoft.com/en-us/library/Dn950146(v=VS.85).aspx">D3D12_MESSAGE_ID</a>.
          


### -field pDescription

The message string.
          


### -field DescriptionByteLength

The length of <i>pDescription</i>, in bytes.
          


## -remarks



This structure is returned from <a href="https://msdn.microsoft.com/en-us/library/Dn950174(v=VS.85).aspx">ID3D12InfoQueue::GetMessage</a> as part of the Information Queue feature (see <a href="https://msdn.microsoft.com/en-us/library/Dn950163(v=VS.85).aspx">ID3D12InfoQueue</a>).






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950152(v=VS.85).aspx">Debug Layer Structures</a>
 

 

