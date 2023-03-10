---
UID: NS:d3d10.D3D10_SO_DECLARATION_ENTRY
title: D3D10_SO_DECLARATION_ENTRY (d3d10.h)
description: Description of a vertex element in a vertex buffer in an output slot. (D3D10_SO_DECLARATION_ENTRY)
helpviewer_keywords: ["367a5fa7-5907-24fc-2124-92ee48f50140","D3D10_SO_DECLARATION_ENTRY","D3D10_SO_DECLARATION_ENTRY structure [Direct3D 10]","d3d10/D3D10_SO_DECLARATION_ENTRY","direct3d10.d3d10_so_declaration_entry"]
old-location: direct3d10\d3d10_so_declaration_entry.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_so_declaration_entry.htm
ms.date: 12/05/2018
ms.keywords: 367a5fa7-5907-24fc-2124-92ee48f50140, D3D10_SO_DECLARATION_ENTRY, D3D10_SO_DECLARATION_ENTRY structure [Direct3D 10], d3d10/D3D10_SO_DECLARATION_ENTRY, direct3d10.d3d10_so_declaration_entry
req.header: d3d10.h
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
req.typenames: D3D10_SO_DECLARATION_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_SO_DECLARATION_ENTRY
 - d3d10/D3D10_SO_DECLARATION_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_SO_DECLARATION_ENTRY
---

# D3D10_SO_DECLARATION_ENTRY structure


## -description

Description of a vertex element in a vertex buffer in an output slot.

## -struct-fields

### -field SemanticName

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Type of output element.  Possible values: "POSITION", "NORMAL", or "TEXCOORD0".

### -field SemanticIndex

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Output element's zero-based index. Should be used if, for example, you have more than one texture coordinate stored in each vertex.

### -field StartComponent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Which component of the entry to begin writing out to. Valid values are 0 ~ 3. For example, if you only wish to output to the y and z components of a position, then StartComponent should be 1 and ComponentCount should be 2.

### -field ComponentCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The number of components of the entry to write out to. Valid values are 1 ~ 4. For example, if you only wish to output to the y and z components of a position, then StartComponent should be 1 and ComponentCount should be 2.

### -field OutputSlot

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The output slot that contains the vertex buffer that contains this output entry.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>
