---
UID: NS:d3d12.D3D12_COMMAND_SIGNATURE_DESC
title: D3D12_COMMAND_SIGNATURE_DESC (d3d12.h)
description: Describes the arguments (parameters) of a command signature.
helpviewer_keywords: ["D3D12_COMMAND_SIGNATURE_DESC","D3D12_COMMAND_SIGNATURE_DESC structure","d3d12/D3D12_COMMAND_SIGNATURE_DESC","direct3d12.d3d12_command_signature_desc"]
old-location: direct3d12\d3d12_command_signature_desc.htm
tech.root: direct3d12
ms.assetid: 3ACB1582-7A93-4D8D-A463-A828EF0C7F92
ms.date: 12/05/2018
ms.keywords: D3D12_COMMAND_SIGNATURE_DESC, D3D12_COMMAND_SIGNATURE_DESC structure, d3d12/D3D12_COMMAND_SIGNATURE_DESC, direct3d12.d3d12_command_signature_desc
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D12_COMMAND_SIGNATURE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_COMMAND_SIGNATURE_DESC
 - d3d12/D3D12_COMMAND_SIGNATURE_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_COMMAND_SIGNATURE_DESC
---

# D3D12_COMMAND_SIGNATURE_DESC structure


## -description

Describes the arguments (parameters) of a command signature.

## -struct-fields

### -field ByteStride

Specifies the size of each command in the drawing buffer, in bytes.

### -field NumArgumentDescs

Specifies the number of arguments in the command signature.

### -field pArgumentDescs

An array of <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc">D3D12_INDIRECT_ARGUMENT_DESC</a> structures,
            containing details of the arguments, including whether the argument is a vertex buffer, constant, constant buffer view, shader resource view, or unordered access view.

### -field NodeMask

For single GPU operation, set this to zero. If there are multiple GPU nodes, set bits to identify the nodes (the  device's physical adapters) for which the command signature is to apply.
            Each bit in the mask corresponds to a single node.
            Refer to <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.

## -remarks

Use this structure by <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature">CreateCommandSignature</a>.

## -see-also

<a href="/windows/win32/direct3d12/direct3d-12-structures">Core Structures</a>

