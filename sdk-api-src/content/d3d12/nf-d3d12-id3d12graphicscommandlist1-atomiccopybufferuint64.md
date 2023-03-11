---
UID: NF:d3d12.ID3D12GraphicsCommandList1.AtomicCopyBufferUINT64
title: ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64 (d3d12.h)
description: Atomically copies a primary data element of type UINT64 from one resource to another, along with optional dependent resources.
helpviewer_keywords: ["AtomicCopyBufferUINT64","AtomicCopyBufferUINT64 method","AtomicCopyBufferUINT64 method","ID3D12GraphicsCommandList1 interface","ID3D12GraphicsCommandList1 interface","AtomicCopyBufferUINT64 method","ID3D12GraphicsCommandList1.AtomicCopyBufferUINT64","ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64","d3d12/ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64","direct3d12.id3d12graphicscommandlist1_atomiccopybufferuint64"]
old-location: direct3d12\id3d12graphicscommandlist1_atomiccopybufferuint64.htm
tech.root: direct3d12
ms.assetid: F83870E9-5256-4A3E-BAF7-05C4CCB28442
ms.date: 08/10/2022
ms.keywords: AtomicCopyBufferUINT64, AtomicCopyBufferUINT64 method, AtomicCopyBufferUINT64 method,ID3D12GraphicsCommandList1 interface, ID3D12GraphicsCommandList1 interface,AtomicCopyBufferUINT64 method, ID3D12GraphicsCommandList1.AtomicCopyBufferUINT64, ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64, d3d12/ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64, direct3d12.id3d12graphicscommandlist1_atomiccopybufferuint64
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64
 - d3d12/ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList1.AtomicCopyBufferUINT64
---

# ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64


## -description

Atomically copies a primary data element of type UINT64 from one resource to another, along with optional dependent resources.

These 'dependent resources' are so-named because they depend upon the primary data element to locate them, typically the key element is an address, index, or other handle that refers to one or more the dependent resources indirectly. 

This function supports a primary data element of type UINT64 (64bit). A different version of this function, <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint">AtomicCopyBufferUINT</a>, supports a primary data element of type UINT (32bit).

## -parameters

### -param pDstBuffer [in]

Type: <b>ID3D12Resource*</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values?view=vs-2015">SAL</a>: <code>_In_</code>

The resource that the UINT64 primary data element is copied into.

### -param DstOffset

Type: <b>UINT64</b>

An offset into the destination resource buffer that specifies where the primary data element is copied into, in bytes. This offset combined with the base address of the resource buffer must result in a memory address that's naturally aligned for UINT64 values.

### -param pSrcBuffer [in]

Type: <b>ID3D12Resource*</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

The resource that the UINT64 primary data element is copied from. This data is typically an address, index, or other handle that shader code can use to locate the most-recent version of latency-sensitive information.

### -param SrcOffset

Type: <b>UINT64</b>

An offset into the source resource buffer that specifies where the primary data element is copied from, in bytes. This offset combined with the base address of the resource buffer must result in a memory address that's naturally aligned for UINT64 values.

### -param Dependencies

Type: <b>UINT</b>

The number of dependent resources.

### -param ppDependentResources [in]

Type: <b>ID3D12Resource*</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_reads_(Dependencies)</code>

An array of resources that contain the dependent elements of the data payload.

### -param pDependentSubresourceRanges [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64">D3D12_SUBRESOURCE_RANGE_UINT64</a>*</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_reads_(Dependencies)</code>

An array of subresource ranges that specify the dependent elements of the data payload. These elements are completely updated before the primary data element is itself atomically copied. This ensures that the entire operation is logically atomic; that is, the primary data element never refers to an incomplete data payload.

## -remarks

This method is typically used to update resources for which normal rendering pipeline latency can be detrimental to user experience. For example, an application can compute a view matrix from the latest user input (such as from the sensors of a head-mounted display), and use this function to update and activate this matrix in command lists already dispatched to the GPU to reduce perceived latency between input and rendering.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist1">ID3D12GraphicsCommandList1</a>