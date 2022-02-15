---
UID: NS:directml.DML_BUFFER_BINDING
title: DML_BUFFER_BINDING
description: Specifies a resource binding described by a range of bytes in a Direct3D 12 buffer, represented by an offset and size into an ID3D12Resource.
helpviewer_keywords: ["DML_BUFFER_BINDING","DML_BUFFER_BINDING structure","direct3d12.dml_buffer_binding","directml/DML_BUFFER_BINDING"]
old-location: direct3d12\dml_buffer_binding.htm
tech.root: directml
ms.assetid: 05BF22D6-D660-4A80-AFE3-27D7BF2D8BDE
ms.date: 12/5/2018
req.header: directml.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DML_BUFFER_BINDING
 - directml/DML_BUFFER_BINDING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_BUFFER_BINDING
---

## -description

Specifies a resource binding described by a range of bytes in a Direct3D 12 buffer, represented by an offset and size into an <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>.

## -struct-fields

### -field Buffer

Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>*</b>

An optional pointer to an <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> interface representing a buffer. The resource must have dimension <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension">D3D12_RESOURCE_DIMENSION_BUFFER</a>, and the
      range described by this struct must lie within the bounds of the buffer. You may supply <b>nullptr</b> for this member to indicate 'no binding'.

### -field Offset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

The offset, in bytes, from the start of the buffer where the range begins. This offset must be aligned to a
      multiple of [DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT](/windows/desktop/direct3d12/direct3d-directml-constants) or the <b>GuaranteedBaseOffsetAlignment</b> supplied as part of the
      [DML_BUFFER_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_buffer_tensor_desc).

### -field SizeInBytes

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

The size of the range, in bytes.

## -see-also

<a href="/windows/ai/directml/dml-binding">Binding in DirectML</a>
