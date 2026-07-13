---
UID: NE:d3d12sdklayers.D3D12_MESSAGE_CATEGORY
title: D3D12_MESSAGE_CATEGORY (d3d12sdklayers.h)
description: Specifies categories of debug messages.
helpviewer_keywords: ["D3D12_MESSAGE_CATEGORY","D3D12_MESSAGE_CATEGORY enumeration","D3D12_MESSAGE_CATEGORY_APPLICATION_DEFINED","D3D12_MESSAGE_CATEGORY_CLEANUP","D3D12_MESSAGE_CATEGORY_COMPILATION","D3D12_MESSAGE_CATEGORY_EXECUTION","D3D12_MESSAGE_CATEGORY_INITIALIZATION","D3D12_MESSAGE_CATEGORY_MISCELLANEOUS","D3D12_MESSAGE_CATEGORY_RESOURCE_MANIPULATION","D3D12_MESSAGE_CATEGORY_SHADER","D3D12_MESSAGE_CATEGORY_STATE_CREATION","D3D12_MESSAGE_CATEGORY_STATE_GETTING","D3D12_MESSAGE_CATEGORY_STATE_SETTING","d3d12sdklayers/D3D12_MESSAGE_CATEGORY","d3d12sdklayers/D3D12_MESSAGE_CATEGORY_APPLICATION_DEFINED","d3d12sdklayers/D3D12_MESSAGE_CATEGORY_CLEANUP","d3d12sdklayers/D3D12_MESSAGE_CATEGORY_COMPILATION","d3d12sdklayers/D3D12_MESSAGE_CATEGORY_EXECUTION","d3d12sdklayers/D3D12_MESSAGE_CATEGORY_INITIALIZATION","d3d12sdklayers/D3D12_MESSAGE_CATEGORY_MISCELLANEOUS","d3d12sdklayers/D3D12_MESSAGE_CATEGORY_RESOURCE_MANIPULATION","d3d12sdklayers/D3D12_MESSAGE_CATEGORY_SHADER","d3d12sdklayers/D3D12_MESSAGE_CATEGORY_STATE_CREATION","d3d12sdklayers/D3D12_MESSAGE_CATEGORY_STATE_GETTING","d3d12sdklayers/D3D12_MESSAGE_CATEGORY_STATE_SETTING","direct3d12.d3d12_message_category"]
old-location: direct3d12\d3d12_message_category.htm
tech.root: direct3d12
ms.assetid: 297923A3-CE6A-46AF-B8B6-E2AE0C1920CC
ms.date: 12/05/2018
ms.keywords: D3D12_MESSAGE_CATEGORY, D3D12_MESSAGE_CATEGORY enumeration, D3D12_MESSAGE_CATEGORY_APPLICATION_DEFINED, D3D12_MESSAGE_CATEGORY_CLEANUP, D3D12_MESSAGE_CATEGORY_COMPILATION, D3D12_MESSAGE_CATEGORY_EXECUTION, D3D12_MESSAGE_CATEGORY_INITIALIZATION, D3D12_MESSAGE_CATEGORY_MISCELLANEOUS, D3D12_MESSAGE_CATEGORY_RESOURCE_MANIPULATION, D3D12_MESSAGE_CATEGORY_SHADER, D3D12_MESSAGE_CATEGORY_STATE_CREATION, D3D12_MESSAGE_CATEGORY_STATE_GETTING, D3D12_MESSAGE_CATEGORY_STATE_SETTING, d3d12sdklayers/D3D12_MESSAGE_CATEGORY, d3d12sdklayers/D3D12_MESSAGE_CATEGORY_APPLICATION_DEFINED, d3d12sdklayers/D3D12_MESSAGE_CATEGORY_CLEANUP, d3d12sdklayers/D3D12_MESSAGE_CATEGORY_COMPILATION, d3d12sdklayers/D3D12_MESSAGE_CATEGORY_EXECUTION, d3d12sdklayers/D3D12_MESSAGE_CATEGORY_INITIALIZATION, d3d12sdklayers/D3D12_MESSAGE_CATEGORY_MISCELLANEOUS, d3d12sdklayers/D3D12_MESSAGE_CATEGORY_RESOURCE_MANIPULATION, d3d12sdklayers/D3D12_MESSAGE_CATEGORY_SHADER, d3d12sdklayers/D3D12_MESSAGE_CATEGORY_STATE_CREATION, d3d12sdklayers/D3D12_MESSAGE_CATEGORY_STATE_GETTING, d3d12sdklayers/D3D12_MESSAGE_CATEGORY_STATE_SETTING, direct3d12.d3d12_message_category
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
targetos: Windows
req.typenames: D3D12_MESSAGE_CATEGORY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_MESSAGE_CATEGORY
 - d3d12sdklayers/D3D12_MESSAGE_CATEGORY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12sdklayers.h
api_name:
 - D3D12_MESSAGE_CATEGORY
---

# D3D12_MESSAGE_CATEGORY enumeration


## -description

Specifies categories of debug messages. This will identify the category of a message when retrieving a message with <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage">ID3D12InfoQueue::GetMessage</a> and when adding a message with <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage">ID3D12InfoQueue::AddMessage</a>. When creating an info queue filter, these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.

## -enum-fields

### -field D3D12_MESSAGE_CATEGORY_APPLICATION_DEFINED:0

Indicates a user defined message, see <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage">ID3D12InfoQueue::AddMessage</a>.

### -field D3D12_MESSAGE_CATEGORY_MISCELLANEOUS

### -field D3D12_MESSAGE_CATEGORY_INITIALIZATION

### -field D3D12_MESSAGE_CATEGORY_CLEANUP

### -field D3D12_MESSAGE_CATEGORY_COMPILATION

### -field D3D12_MESSAGE_CATEGORY_STATE_CREATION

### -field D3D12_MESSAGE_CATEGORY_STATE_SETTING

### -field D3D12_MESSAGE_CATEGORY_STATE_GETTING

### -field D3D12_MESSAGE_CATEGORY_RESOURCE_MANIPULATION

### -field D3D12_MESSAGE_CATEGORY_EXECUTION

### -field D3D12_MESSAGE_CATEGORY_SHADER

## -remarks

This is part of the Information Queue feature, refer to the <a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a> Interface.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-sdklayers-enumerations">Debug Layer Enumerations</a>
