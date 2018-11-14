---
UID: NS:d3d12sdklayers.D3D12_MESSAGE
title: D3D12_MESSAGE
author: windows-sdk-content
description: A debug message in the Information Queue.
old-location: direct3d12\d3d12_message.htm
tech.root: direct3d12
ms.assetid: DED84AC1-0126-450E-8A0A-1336BB4084D4
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: D3D12_MESSAGE, D3D12_MESSAGE structure, d3d12sdklayers/D3D12_MESSAGE, direct3d12.d3d12_message
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d12sdklayers.h
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
 - d3d12sdklayers.h
api_name:
 - D3D12_MESSAGE
product: Windows
targetos: Windows
req.typenames: D3D12_MESSAGE
req.redist: 
---

# D3D12_MESSAGE structure


## -description


A debug message in the Information Queue.


## -struct-fields




### -field Category

The category of the message. See <a href="https://msdn.microsoft.com/297923A3-CE6A-46AF-B8B6-E2AE0C1920CC">D3D12_MESSAGE_CATEGORY</a>.
          


### -field Severity

The severity of the message. See  <a href="https://msdn.microsoft.com/44D94C37-4BA8-49FC-BEEF-6666AD59B627">D3D12_MESSAGE_SEVERITY</a>.
          


### -field ID

The ID of the message. See <a href="https://msdn.microsoft.com/95681EB0-C00B-42C8-91E1-1D1F657C886B">D3D12_MESSAGE_ID</a>.
          


### -field pDescription

The message string.
          


### -field DescriptionByteLength

The length of <i>pDescription</i>, in bytes.
          


## -remarks



This structure is returned from <a href="https://msdn.microsoft.com/B7B6D1C4-18FD-492A-8346-CA02FCD3EC4B">ID3D12InfoQueue::GetMessage</a> as part of the Information Queue feature (see <a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a>).






## -see-also




<a href="https://msdn.microsoft.com/FE8796A7-98D1-4333-8755-2A47567560B3">Debug Layer Structures</a>
 

 

