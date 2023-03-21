---
UID: NS:d3d11.D3D11_SO_DECLARATION_ENTRY
title: D3D11_SO_DECLARATION_ENTRY (d3d11.h)
description: Description of a vertex element in a vertex buffer in an output slot. (D3D11_SO_DECLARATION_ENTRY)
helpviewer_keywords: ["D3D11_SO_DECLARATION_ENTRY","D3D11_SO_DECLARATION_ENTRY structure [Direct3D 11]","d3d11/D3D11_SO_DECLARATION_ENTRY","direct3d11.d3d11_so_declaration_entry","fdc7503f-19ea-e13f-ae4b-f27469123a78"]
old-location: direct3d11\d3d11_so_declaration_entry.htm
tech.root: direct3d11
ms.assetid: c40e8db6-e26f-4c61-a812-f60eae43e86b
ms.date: 12/05/2018
ms.keywords: D3D11_SO_DECLARATION_ENTRY, D3D11_SO_DECLARATION_ENTRY structure [Direct3D 11], d3d11/D3D11_SO_DECLARATION_ENTRY, direct3d11.d3d11_so_declaration_entry, fdc7503f-19ea-e13f-ae4b-f27469123a78
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
req.typenames: D3D11_SO_DECLARATION_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_SO_DECLARATION_ENTRY
 - d3d11/D3D11_SO_DECLARATION_ENTRY
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
 - D3D11_SO_DECLARATION_ENTRY
---

# D3D11_SO_DECLARATION_ENTRY structure


## -description

Description of a vertex element in a vertex buffer in an output slot.

## -struct-fields

### -field Stream

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based, stream number.

### -field SemanticName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Type of output element; possible values include: <b>"POSITION"</b>, <b>"NORMAL"</b>, or <b>"TEXCOORD0"</b>.
        Note that if <i>SemanticName</i> is <b>NULL</b> then 
        <i>ComponentCount</i> can be greater than 4 and the described entry will be a gap in the stream out where no data will be written.

### -field SemanticIndex

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Output element's zero-based index. Should be used if, for example, you have more than one texture coordinate stored in each vertex.

### -field StartComponent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Which component of the entry to begin writing out to. Valid values are 0 to 3. For example, if you only wish to output to the y and z components 
        of a position, then StartComponent should be 1 and ComponentCount should be 2.

### -field ComponentCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The number of components of the entry to write out to. Valid values are 1 to 4. For example, if you only wish to output to the y and z components 
        of a position, then StartComponent should be 1 and ComponentCount should be 2.  Note that if <i>SemanticName</i> is <b>NULL</b> then 
        <i>ComponentCount</i> can be greater than 4 and the described entry will be a gap in the stream out where no data will be written.

### -field OutputSlot

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The associated stream output buffer that is bound to the pipeline 
        (see <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-sosettargets">ID3D11DeviceContext::SOSetTargets</a>). 
        The valid range for <i>OutputSlot</i> is 0 to 3.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>
