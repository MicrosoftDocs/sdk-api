---
UID: NS:d3d11.D3D11_BUFFER_DESC
title: D3D11_BUFFER_DESC (d3d11.h)
description: Describes a buffer resource. (D3D11_BUFFER_DESC)
helpviewer_keywords: ["D3D11_BUFFER_DESC","D3D11_BUFFER_DESC structure [Direct3D 11]","d2dd6908-ed59-4009-c1dc-5afae3472d02","d3d11/D3D11_BUFFER_DESC","direct3d11.d3d11_buffer_desc"]
old-location: direct3d11\d3d11_buffer_desc.htm
tech.root: direct3d11
ms.assetid: a5e470bb-011b-4a2a-96d6-cbf76fe12638
ms.date: 12/05/2018
ms.keywords: D3D11_BUFFER_DESC, D3D11_BUFFER_DESC structure [Direct3D 11], d2dd6908-ed59-4009-c1dc-5afae3472d02, d3d11/D3D11_BUFFER_DESC, direct3d11.d3d11_buffer_desc
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
req.typenames: D3D11_BUFFER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_BUFFER_DESC
 - d3d11/D3D11_BUFFER_DESC
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
 - D3D11_BUFFER_DESC
---

# D3D11_BUFFER_DESC structure


## -description

Describes a buffer resource.

## -struct-fields

### -field ByteWidth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the buffer in bytes.

### -field Usage

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE</a></b>

Identify how the buffer is expected to be read from and written to. Frequency of update is a key factor. The most common value is typically D3D11_USAGE_DEFAULT; see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE</a> for all possible values.

### -field BindFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Identify how the buffer will be bound to the pipeline. Flags (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_FLAG</a>) can be combined with a bitwise OR.

### -field CPUAccessFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

CPU access flags (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag">D3D11_CPU_ACCESS_FLAG</a>) or 0 if no CPU access is necessary. Flags can be combined with a bitwise OR.

### -field MiscFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Miscellaneous flags (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_FLAG</a>) or 0 if unused. Flags can be combined with a bitwise OR.

### -field StructureByteStride

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size of each element in the buffer structure (in bytes) when the buffer represents a structured buffer. For more info about structured buffers, see <a href="/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources">Structured Buffer</a>.

The size value in <b>StructureByteStride</b> must match the size of the format that you use for views of the buffer. For example, if you use a shader resource view (SRV) to read a buffer in a pixel shader, the SRV format size must match the size value in <b>StructureByteStride</b>.

## -remarks

This structure is used by <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createbuffer">ID3D11Device::CreateBuffer</a> to create buffer resources.

In addition to this structure, you can also use the <a href="/windows/desktop/api/d3d11/ns-d3d11-cd3d11_buffer_desc">CD3D11_BUFFER_DESC</a> derived structure, which is defined  in D3D11.h and behaves like an inherited class, to help create a buffer description.

If the bind flag is <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">D3D11_BIND_CONSTANT_BUFFER</a>, you must set the <b>ByteWidth</b> value in multiples of 16, and less than or equal to <b>D3D11_REQ_CONSTANT_BUFFER_ELEMENT_COUNT</b>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
