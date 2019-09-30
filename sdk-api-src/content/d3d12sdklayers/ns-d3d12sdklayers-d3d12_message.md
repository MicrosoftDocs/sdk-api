---
UID: NS:d3d12sdklayers.D3D12_MESSAGE
title: D3D12_MESSAGE (d3d12sdklayers.h)
author: windows-sdk-content
description: A debug message in the Information Queue.
old-location: direct3d12\d3d12_message.htm
tech.root: direct3d12
ms.assetid: DED84AC1-0126-450E-8A0A-1336BB4084D4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_MESSAGE, D3D12_MESSAGE structure, d3d12sdklayers/D3D12_MESSAGE, direct3d12.d3d12_message
ms.topic: struct
f1_keywords: 
 - "d3d12sdklayers/D3D12_MESSAGE"
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
targetos: Windows
req.typenames: D3D12_MESSAGE
req.redist: 
ms.custom: 19H1
---

# D3D12_MESSAGE structure


## -description


A debug message in the Information Queue.


## -struct-fields




### -field Category

The category of the message. See <a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category">D3D12_MESSAGE_CATEGORY</a>.
          


### -field Severity

The severity of the message. See  <a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity">D3D12_MESSAGE_SEVERITY</a>.
          


### -field ID

The ID of the message. See <a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id">D3D12_MESSAGE_ID</a>.
          


### -field pDescription

The message string.
          


### -field DescriptionByteLength

The length of <i>pDescription</i>, in bytes.
          


## -remarks



This structure is returned from <a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage">ID3D12InfoQueue::GetMessage</a> as part of the Information Queue feature (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>).






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-sdklayers-structures">Debug Layer Structures</a>
 

 

