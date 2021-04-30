---
UID: NS:d3d12.D3D12_SO_DECLARATION_ENTRY
title: D3D12_SO_DECLARATION_ENTRY (d3d12.h)
description: Describes a vertex element in a vertex buffer in an output slot.
helpviewer_keywords: ["D3D12_SO_DECLARATION_ENTRY","D3D12_SO_DECLARATION_ENTRY structure","d3d12/D3D12_SO_DECLARATION_ENTRY","direct3d12.d3d12_so_declaration_entry"]
old-location: direct3d12\d3d12_so_declaration_entry.htm
tech.root: direct3d12
ms.assetid: F16FA746-2213-4F11-85AD-2CDCB0744618
ms.date: 12/05/2018
ms.keywords: D3D12_SO_DECLARATION_ENTRY, D3D12_SO_DECLARATION_ENTRY structure, d3d12/D3D12_SO_DECLARATION_ENTRY, direct3d12.d3d12_so_declaration_entry
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
req.typenames: D3D12_SO_DECLARATION_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_SO_DECLARATION_ENTRY
 - d3d12/D3D12_SO_DECLARATION_ENTRY
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
 - D3D12_SO_DECLARATION_ENTRY
---

# D3D12_SO_DECLARATION_ENTRY structure


## -description

Describes a vertex element in a vertex buffer in an output slot.

## -struct-fields

### -field Stream

Zero-based, stream number.

### -field SemanticName

Type of output element; possible values include: <b>"POSITION"</b>, <b>"NORMAL"</b>, or <b>"TEXCOORD0"</b>.
        Note that if <b>SemanticName</b> is <b>NULL</b> then 
        <b>ComponentCount</b> can be greater than 4 and the described entry will be a gap in the stream out where no data will be written.

### -field SemanticIndex

Output element's zero-based index. Use, for example, if you have more than one texture coordinate stored in each vertex.

### -field StartComponent

The component of the entry to begin writing out to. Valid values are 0 to 3. For example, if you only wish to output to the y and z components 
        of a position, <b>StartComponent</b> is 1 and <b>ComponentCount</b> is 2.

### -field ComponentCount

The number of components of the entry to write out to. Valid values are 1 to 4. For example, if you only wish to output to the y and z components 
        of a position, <b>StartComponent</b> is 1 and <b>ComponentCount</b> is 2.  Note that if <b>SemanticName</b> is <b>NULL</b> then 
        <b>ComponentCount</b> can be greater than 4 and the described entry will be a gap in the stream out where no data will be written.

### -field OutputSlot

The associated stream output buffer that is bound to the pipeline. 
        The valid range for <b>OutputSlot</b> is 0 to 3.

## -remarks

Specify an array of <b>D3D12_SO_DECLARATION_ENTRY</b> structures in the <b>pSODeclaration</b> member of a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc">D3D12_STREAM_OUTPUT_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>