---
UID: NE:d3d11sdklayers.D3D11_MESSAGE_CATEGORY
title: D3D11_MESSAGE_CATEGORY
author: windows-sdk-content
description: Categories of debug messages.
old-location: direct3d11\d3d11_message_category.htm
tech.root: direct3d11
ms.assetid: e4af5bf6-cbbe-488a-ad8e-3a4409f2591d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 2ba52fac-75ec-4d76-4f85-c3a01fddd778, D3D11_MESSAGE_CATEGORY, D3D11_MESSAGE_CATEGORY enumeration [Direct3D 11], D3D11_MESSAGE_CATEGORY_APPLICATION_DEFINED, D3D11_MESSAGE_CATEGORY_CLEANUP, D3D11_MESSAGE_CATEGORY_COMPILATION, D3D11_MESSAGE_CATEGORY_EXECUTION, D3D11_MESSAGE_CATEGORY_INITIALIZATION, D3D11_MESSAGE_CATEGORY_MISCELLANEOUS, D3D11_MESSAGE_CATEGORY_RESOURCE_MANIPULATION, D3D11_MESSAGE_CATEGORY_SHADER, D3D11_MESSAGE_CATEGORY_STATE_CREATION, D3D11_MESSAGE_CATEGORY_STATE_GETTING, D3D11_MESSAGE_CATEGORY_STATE_SETTING, d3d11sdklayers/D3D11_MESSAGE_CATEGORY, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_APPLICATION_DEFINED, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_CLEANUP, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_COMPILATION, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_EXECUTION, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_INITIALIZATION, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_MISCELLANEOUS, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_RESOURCE_MANIPULATION, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_SHADER, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_STATE_CREATION, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_STATE_GETTING, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_STATE_SETTING, direct3d11.d3d11_message_category
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - D3D11_MESSAGE_CATEGORY
product: Windows
targetos: Windows
req.typenames: D3D11_MESSAGE_CATEGORY
req.redist: 
---

# D3D11_MESSAGE_CATEGORY enumeration


## -description


Categories of debug messages. This will identify the category of a message when retrieving a message with <a href="https://msdn.microsoft.com/685cddc5-cedd-410f-a693-665d2d69402e">ID3D11InfoQueue::GetMessage</a> and when adding a message with <a href="https://msdn.microsoft.com/7265a273-327a-482b-9d47-6931e031cff8">ID3D11InfoQueue::AddMessage</a>. When creating an <a href="https://msdn.microsoft.com/6ff12751-86dd-4ae0-b532-661a70dad21f">info queue filter</a>, these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.


## -enum-fields




### -field D3D11_MESSAGE_CATEGORY_APPLICATION_DEFINED

User defined message. See <a href="https://msdn.microsoft.com/7265a273-327a-482b-9d47-6931e031cff8">ID3D11InfoQueue::AddMessage</a>.


### -field D3D11_MESSAGE_CATEGORY_MISCELLANEOUS


### -field D3D11_MESSAGE_CATEGORY_INITIALIZATION


### -field D3D11_MESSAGE_CATEGORY_CLEANUP


### -field D3D11_MESSAGE_CATEGORY_COMPILATION


### -field D3D11_MESSAGE_CATEGORY_STATE_CREATION


### -field D3D11_MESSAGE_CATEGORY_STATE_SETTING


### -field D3D11_MESSAGE_CATEGORY_STATE_GETTING


### -field D3D11_MESSAGE_CATEGORY_RESOURCE_MANIPULATION


### -field D3D11_MESSAGE_CATEGORY_EXECUTION


### -field D3D11_MESSAGE_CATEGORY_SHADER

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


## -remarks



This is part of the Information Queue feature. See <a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>.




## -see-also




<a href="https://msdn.microsoft.com/0fd0456b-2638-4b4c-8a34-a3e104a1a034">Layer Enumerations</a>
 

 

