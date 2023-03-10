---
UID: NS:d3d10.D3D10_BUFFER_DESC
title: D3D10_BUFFER_DESC (d3d10.h)
description: Describes a buffer resource. (D3D10_BUFFER_DESC)
helpviewer_keywords: ["1eca8f2f-7776-2027-7a51-209cc4fd7200","CD3D10_BUFFER_DESC","D3D10_BUFFER_DESC","D3D10_BUFFER_DESC structure [Direct3D 10]","d3d10/D3D10_BUFFER_DESC","direct3d10.d3d10_buffer_desc"]
old-location: direct3d10\d3d10_buffer_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_buffer_desc.htm
ms.date: 12/05/2018
ms.keywords: 1eca8f2f-7776-2027-7a51-209cc4fd7200, CD3D10_BUFFER_DESC, D3D10_BUFFER_DESC, D3D10_BUFFER_DESC structure [Direct3D 10], d3d10/D3D10_BUFFER_DESC, direct3d10.d3d10_buffer_desc
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
req.typenames: D3D10_BUFFER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_BUFFER_DESC
 - d3d10/D3D10_BUFFER_DESC
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
 - D3D10_BUFFER_DESC
---

## -description

Describes a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">buffer</a> resource.

## -struct-fields

### -field ByteWidth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the buffer in bytes.

### -field Usage

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">D3D10_USAGE</a></b>

Identify how the buffer is expected to be read from and written to. Frequency of update is a key factor. The most common value is typically D3D10_USAGE_DEFAULT; see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">D3D10_USAGE</a> for all possible values.

### -field BindFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Identify how the buffer will be bound to the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages">pipeline</a>. Applications can logically OR flags together (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag">D3D10_BIND_FLAG</a>) to indicate that the buffer can be accessed in different ways.

### -field CPUAccessFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

CPU access flags (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_cpu_access_flag">D3D10_CPU_ACCESS_FLAG</a>) or 0 if no CPU access is necessary. Applications can logically OR flags together.

### -field MiscFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Miscellaneous flags (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag">D3D10_RESOURCE_MISC_FLAG</a>) or 0 if unused. Applications can logically OR flags together.

## -remarks

This structure is used by <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createbuffer">ID3D10Device::CreateBuffer</a> to create buffer resources.

In addition to this structure, there is also a derived structure in D3D10.h (CD3D10_BUFFER_DESC) which behaves like an inherited class to help create a buffer description.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource structures</a>
