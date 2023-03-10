---
UID: NF:d3d12.ID3D12StateObjectProperties.GetShaderIdentifier
title: ID3D12StateObjectProperties::GetShaderIdentifier (d3d12.h)
description: Retrieves the unique identifier for a shader that can be used in a shader record.
helpviewer_keywords: ["GetShaderIdentifier","GetShaderIdentifier method","GetShaderIdentifier method","ID3D12StateObjectProperties interface","ID3D12StateObjectProperties interface","GetShaderIdentifier method","ID3D12StateObjectProperties.GetShaderIdentifier","ID3D12StateObjectProperties::GetShaderIdentifier","d3d12/ID3D12StateObjectProperties::GetShaderIdentifier","direct3d12.id3d12stateobjectproperties_getshaderidentifier"]
old-location: direct3d12\id3d12stateobjectproperties_getshaderidentifier.htm
tech.root: direct3d12
ms.assetid: E93279A1-4238-49C7-8525-EE01999454D9
ms.date: 12/05/2018
ms.keywords: GetShaderIdentifier, GetShaderIdentifier method, GetShaderIdentifier method,ID3D12StateObjectProperties interface, ID3D12StateObjectProperties interface,GetShaderIdentifier method, ID3D12StateObjectProperties.GetShaderIdentifier, ID3D12StateObjectProperties::GetShaderIdentifier, d3d12/ID3D12StateObjectProperties::GetShaderIdentifier, direct3d12.id3d12stateobjectproperties_getshaderidentifier
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12StateObjectProperties::GetShaderIdentifier
 - d3d12/ID3D12StateObjectProperties::GetShaderIdentifier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12StateObjectProperties.GetShaderIdentifier
---

# ID3D12StateObjectProperties::GetShaderIdentifier


## -description

Retrieves the unique identifier for a shader that can be used in a shader record.

## -parameters

### -param pExportName

Entrypoint in the state object for which to retrieve an identifier.

## -returns

A pointer to the shader identifier.

The data referenced by this pointer is valid as long as the state object it came from is valid.  The size of the data returned is <a href="/windows/desktop/direct3d12/constants">D3D12_SHADER_IDENTIFIER_SIZE_IN_BYTES</a>.  Applications should copy and cache this data to avoid the cost of searching for it in the state object if it will need to be retrieved many times.  The identifier is used in shader records within shader tables in GPU memory, which the app must populate. 

The data itself globally identifies the shader, so even if the shader appears in a different state object with same associations, like any root signatures, it will have the same identifier.

If the shader isn’t fully resolved in the state object, the return value is <b>nullptr</b>.

## -see-also

<a href="../d3d12/nn-d3d12-id3d12stateobjectproperties.md">ID3D12StateObjectProperties</a>
