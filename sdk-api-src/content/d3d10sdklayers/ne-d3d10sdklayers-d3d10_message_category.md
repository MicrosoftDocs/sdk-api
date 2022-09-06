---
UID: NE:d3d10sdklayers.D3D10_MESSAGE_CATEGORY
title: D3D10_MESSAGE_CATEGORY (d3d10sdklayers.h)
description: Categories of debug messages.
helpviewer_keywords: ["6e6b50e6-ab2a-be66-c2cd-8a6cb8f2e2a4","D3D10_MESSAGE_CATEGORY","D3D10_MESSAGE_CATEGORY enumeration [Direct3D 10]","D3D10_MESSAGE_CATEGORY_APPLICATION_DEFINED","D3D10_MESSAGE_CATEGORY_CLEANUP","D3D10_MESSAGE_CATEGORY_COMPILATION","D3D10_MESSAGE_CATEGORY_EXECUTION","D3D10_MESSAGE_CATEGORY_INITIALIZATION","D3D10_MESSAGE_CATEGORY_MISCELLANEOUS","D3D10_MESSAGE_CATEGORY_RESOURCE_MANIPULATION","D3D10_MESSAGE_CATEGORY_STATE_CREATION","D3D10_MESSAGE_CATEGORY_STATE_GETTING","D3D10_MESSAGE_CATEGORY_STATE_SETTING","d3d10sdklayers/D3D10_MESSAGE_CATEGORY","d3d10sdklayers/D3D10_MESSAGE_CATEGORY_APPLICATION_DEFINED","d3d10sdklayers/D3D10_MESSAGE_CATEGORY_CLEANUP","d3d10sdklayers/D3D10_MESSAGE_CATEGORY_COMPILATION","d3d10sdklayers/D3D10_MESSAGE_CATEGORY_EXECUTION","d3d10sdklayers/D3D10_MESSAGE_CATEGORY_INITIALIZATION","d3d10sdklayers/D3D10_MESSAGE_CATEGORY_MISCELLANEOUS","d3d10sdklayers/D3D10_MESSAGE_CATEGORY_RESOURCE_MANIPULATION","d3d10sdklayers/D3D10_MESSAGE_CATEGORY_STATE_CREATION","d3d10sdklayers/D3D10_MESSAGE_CATEGORY_STATE_GETTING","d3d10sdklayers/D3D10_MESSAGE_CATEGORY_STATE_SETTING","direct3d10.d3d10_message_category"]
old-location: direct3d10\d3d10_message_category.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_message_category.htm
ms.date: 12/05/2018
ms.keywords: 6e6b50e6-ab2a-be66-c2cd-8a6cb8f2e2a4, D3D10_MESSAGE_CATEGORY, D3D10_MESSAGE_CATEGORY enumeration [Direct3D 10], D3D10_MESSAGE_CATEGORY_APPLICATION_DEFINED, D3D10_MESSAGE_CATEGORY_CLEANUP, D3D10_MESSAGE_CATEGORY_COMPILATION, D3D10_MESSAGE_CATEGORY_EXECUTION, D3D10_MESSAGE_CATEGORY_INITIALIZATION, D3D10_MESSAGE_CATEGORY_MISCELLANEOUS, D3D10_MESSAGE_CATEGORY_RESOURCE_MANIPULATION, D3D10_MESSAGE_CATEGORY_STATE_CREATION, D3D10_MESSAGE_CATEGORY_STATE_GETTING, D3D10_MESSAGE_CATEGORY_STATE_SETTING, d3d10sdklayers/D3D10_MESSAGE_CATEGORY, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_APPLICATION_DEFINED, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_CLEANUP, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_COMPILATION, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_EXECUTION, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_INITIALIZATION, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_MISCELLANEOUS, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_RESOURCE_MANIPULATION, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_STATE_CREATION, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_STATE_GETTING, d3d10sdklayers/D3D10_MESSAGE_CATEGORY_STATE_SETTING, direct3d10.d3d10_message_category
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
targetos: Windows
req.typenames: D3D10_MESSAGE_CATEGORY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_MESSAGE_CATEGORY
 - d3d10sdklayers/D3D10_MESSAGE_CATEGORY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10sdklayers.h
api_name:
 - D3D10_MESSAGE_CATEGORY
---

# D3D10_MESSAGE_CATEGORY enumeration


## -description

Categories of debug messages. This will identify the category of a message when retrieving a message with <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage">ID3D10InfoQueue::GetMessage</a> and when adding a message with <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10infoqueue-addmessage">ID3D10InfoQueue::AddMessage</a>. When creating an <a href="/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter">info queue filter</a>, these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.

## -enum-fields

### -field D3D10_MESSAGE_CATEGORY_APPLICATION_DEFINED:0

User defined message. See <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10infoqueue-addmessage">ID3D10InfoQueue::AddMessage</a>.

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

This is part of the Information Queue feature. See <a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
