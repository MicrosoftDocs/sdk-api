---
UID: NE:d3d10sdklayers.D3D10_MESSAGE_CATEGORY
title: D3D10_MESSAGE_CATEGORY
author: windows-sdk-content
description: Categories of debug messages.
old-location: direct3d10\d3d10_message_category.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_message_category.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 6e6b50e6-ab2a-be66-c2cd-8a6cb8f2e2a4, D3D10_MESSAGE_CATEGORY, D3D10_MESSAGE_CATEGORY enumeration [Direct3D 10], D3D10_MESSAGE_CATEGORY_APPLICATION_DEFINED, D3D10_MESSAGE_CATEGORY_CLEANUP, D3D10_MESSAGE_CATEGORY_COMPILATION, D3D10_MESSAGE_CATEGORY_EXECUTION, D3D10_MESSAGE_CATEGORY_INITIALIZATION, D3D10_MESSAGE_CATEGORY_MISCELLANEOUS, D3D10_MESSAGE_CATEGORY_RESOURCE_MANIPULATION, D3D10_MESSAGE_CATEGORY_STATE_CREATION, D3D10_MESSAGE_CATEGORY_STATE_GETTING, D3D10_MESSAGE_CATEGORY_STATE_SETTING, d3d10sdklayers/D3D10_MESSAGE_CATEGORY, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_APPLICATION_DEFINED, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_CLEANUP, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_COMPILATION, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_EXECUTION, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_INITIALIZATION, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_MISCELLANEOUS, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_RESOURCE_MANIPULATION, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_STATE_CREATION, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_STATE_GETTING, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_STATE_SETTING, direct3d10.d3d10_message_category
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d10sdklayers.h
req.include-header: D3D10.h
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
 - d3d10sdklayers.h
api_name:
 - D3D10_MESSAGE_CATEGORY
product: Windows
targetos: Windows
req.typenames: D3D10_MESSAGE_CATEGORY
req.redist: 
---

# D3D10_MESSAGE_CATEGORY enumeration


## -description


Categories of debug messages. This will identify the category of a message when retrieving a message with <a href="https://msdn.microsoft.com/c7ed2819-d726-4719-b46c-03c001b9b40d">ID3D10InfoQueue::GetMessage</a> and when adding a message with <a href="https://msdn.microsoft.com/d31a0c87-b895-49e2-96e6-1df68db3995b">ID3D10InfoQueue::AddMessage</a>. When creating an <a href="https://msdn.microsoft.com/78eb4b2c-ec22-4d30-befc-bf253d8768ba">info queue filter</a>, these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.


## -enum-fields




### -field D3D10_MESSAGE_CATEGORY_APPLICATION_DEFINED

User defined message. See <a href="https://msdn.microsoft.com/d31a0c87-b895-49e2-96e6-1df68db3995b">ID3D10InfoQueue::AddMessage</a>.


### -field D3D10_MESSAGE_CATEGORY_MISCELLANEOUS


### -field D3D10_MESSAGE_CATEGORY_INITIALIZATION


### -field D3D10_MESSAGE_CATEGORY_CLEANUP


### -field D3D10_MESSAGE_CATEGORY_COMPILATION


### -field D3D10_MESSAGE_CATEGORY_STATE_CREATION


### -field D3D10_MESSAGE_CATEGORY_STATE_SETTING


### -field D3D10_MESSAGE_CATEGORY_STATE_GETTING


### -field D3D10_MESSAGE_CATEGORY_RESOURCE_MANIPULATION


### -field D3D10_MESSAGE_CATEGORY_EXECUTION


### -field D3D10_MESSAGE_CATEGORY_SHADER




## -remarks



This is part of the Information Queue feature. See <a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>.




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

