---
UID: NE:d3d11.D3D11_DEVICE_CONTEXT_TYPE
title: D3D11_DEVICE_CONTEXT_TYPE (d3d11.h)
description: Device context options.
helpviewer_keywords: ["04cb26d8-2f58-6bc4-0362-f5112e175882","D3D11_DEVICE_CONTEXT_DEFERRED","D3D11_DEVICE_CONTEXT_IMMEDIATE","D3D11_DEVICE_CONTEXT_TYPE","D3D11_DEVICE_CONTEXT_TYPE enumeration [Direct3D 11]","d3d11/D3D11_DEVICE_CONTEXT_DEFERRED","d3d11/D3D11_DEVICE_CONTEXT_IMMEDIATE","d3d11/D3D11_DEVICE_CONTEXT_TYPE","direct3d11.d3d11_device_context_type"]
old-location: direct3d11\d3d11_device_context_type.htm
tech.root: direct3d11
ms.assetid: 1c2e6ed9-63d5-4ea0-bd98-7604c0ee7021
ms.date: 12/05/2018
ms.keywords: 04cb26d8-2f58-6bc4-0362-f5112e175882, D3D11_DEVICE_CONTEXT_DEFERRED, D3D11_DEVICE_CONTEXT_IMMEDIATE, D3D11_DEVICE_CONTEXT_TYPE, D3D11_DEVICE_CONTEXT_TYPE enumeration [Direct3D 11], d3d11/D3D11_DEVICE_CONTEXT_DEFERRED, d3d11/D3D11_DEVICE_CONTEXT_IMMEDIATE, d3d11/D3D11_DEVICE_CONTEXT_TYPE, direct3d11.d3d11_device_context_type
req.header: d3d11.h
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
req.typenames: D3D11_DEVICE_CONTEXT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_DEVICE_CONTEXT_TYPE
 - d3d11/D3D11_DEVICE_CONTEXT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_DEVICE_CONTEXT_TYPE
---

# D3D11_DEVICE_CONTEXT_TYPE enumeration


## -description

Device context options.

## -enum-fields

### -field D3D11_DEVICE_CONTEXT_IMMEDIATE:0

The device context is an immediate context.

### -field D3D11_DEVICE_CONTEXT_DEFERRED

The device context is a deferred context.

## -remarks

This enumeration is used by <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gettype">ID3D11DeviceContext::GetType</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>
