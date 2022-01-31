---
UID: NE:d3d11sdklayers.D3D11_MESSAGE_CATEGORY
title: D3D11_MESSAGE_CATEGORY (d3d11sdklayers.h)
description: Categories of debug messages.
helpviewer_keywords: ["2ba52fac-75ec-4d76-4f85-c3a01fddd778","D3D11_MESSAGE_CATEGORY","D3D11_MESSAGE_CATEGORY enumeration [Direct3D 11]","D3D11_MESSAGE_CATEGORY_APPLICATION_DEFINED","D3D11_MESSAGE_CATEGORY_CLEANUP","D3D11_MESSAGE_CATEGORY_COMPILATION","D3D11_MESSAGE_CATEGORY_EXECUTION","D3D11_MESSAGE_CATEGORY_INITIALIZATION","D3D11_MESSAGE_CATEGORY_MISCELLANEOUS","D3D11_MESSAGE_CATEGORY_RESOURCE_MANIPULATION","D3D11_MESSAGE_CATEGORY_SHADER","D3D11_MESSAGE_CATEGORY_STATE_CREATION","D3D11_MESSAGE_CATEGORY_STATE_GETTING","D3D11_MESSAGE_CATEGORY_STATE_SETTING","d3d11sdklayers/D3D11_MESSAGE_CATEGORY","d3d11sdklayers/D3D11_MESSAGE_CATEGORY_APPLICATION_DEFINED","d3d11sdklayers/D3D11_MESSAGE_CATEGORY_CLEANUP","d3d11sdklayers/D3D11_MESSAGE_CATEGORY_COMPILATION","d3d11sdklayers/D3D11_MESSAGE_CATEGORY_EXECUTION","d3d11sdklayers/D3D11_MESSAGE_CATEGORY_INITIALIZATION","d3d11sdklayers/D3D11_MESSAGE_CATEGORY_MISCELLANEOUS","d3d11sdklayers/D3D11_MESSAGE_CATEGORY_RESOURCE_MANIPULATION","d3d11sdklayers/D3D11_MESSAGE_CATEGORY_SHADER","d3d11sdklayers/D3D11_MESSAGE_CATEGORY_STATE_CREATION","d3d11sdklayers/D3D11_MESSAGE_CATEGORY_STATE_GETTING","d3d11sdklayers/D3D11_MESSAGE_CATEGORY_STATE_SETTING","direct3d11.d3d11_message_category"]
old-location: direct3d11\d3d11_message_category.htm
tech.root: direct3d11
ms.assetid: e4af5bf6-cbbe-488a-ad8e-3a4409f2591d
ms.date: 12/05/2018
ms.keywords: 2ba52fac-75ec-4d76-4f85-c3a01fddd778, D3D11_MESSAGE_CATEGORY, D3D11_MESSAGE_CATEGORY enumeration [Direct3D 11], D3D11_MESSAGE_CATEGORY_APPLICATION_DEFINED, D3D11_MESSAGE_CATEGORY_CLEANUP, D3D11_MESSAGE_CATEGORY_COMPILATION, D3D11_MESSAGE_CATEGORY_EXECUTION, D3D11_MESSAGE_CATEGORY_INITIALIZATION, D3D11_MESSAGE_CATEGORY_MISCELLANEOUS, D3D11_MESSAGE_CATEGORY_RESOURCE_MANIPULATION, D3D11_MESSAGE_CATEGORY_SHADER, D3D11_MESSAGE_CATEGORY_STATE_CREATION, D3D11_MESSAGE_CATEGORY_STATE_GETTING, D3D11_MESSAGE_CATEGORY_STATE_SETTING, d3d11sdklayers/D3D11_MESSAGE_CATEGORY, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_APPLICATION_DEFINED, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_CLEANUP, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_COMPILATION, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_EXECUTION, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_INITIALIZATION, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_MISCELLANEOUS, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_RESOURCE_MANIPULATION, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_SHADER, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_STATE_CREATION, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_STATE_GETTING, d3d11sdklayers/D3D11_MESSAGE_CATEGORY_STATE_SETTING, direct3d11.d3d11_message_category
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
targetos: Windows
req.typenames: D3D11_MESSAGE_CATEGORY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_MESSAGE_CATEGORY
 - d3d11sdklayers/D3D11_MESSAGE_CATEGORY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11SDKLayers.h
api_name:
 - D3D11_MESSAGE_CATEGORY
---

# D3D11_MESSAGE_CATEGORY enumeration


## -description

Categories of debug messages. This will identify the category of a message when retrieving a message with <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage">ID3D11InfoQueue::GetMessage</a> and when adding a message with <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage">ID3D11InfoQueue::AddMessage</a>. When creating an <a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_info_queue_filter">info queue filter</a>, these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.

## -enum-fields

### -field D3D11_MESSAGE_CATEGORY_APPLICATION_DEFINED:0

User defined message. See <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage">ID3D11InfoQueue::AddMessage</a>.

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

This is part of the Information Queue feature. See <a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-enums">Layer Enumerations</a>
