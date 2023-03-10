---
UID: NF:d3d12.ID3D12GraphicsCommandList1.SetSamplePositions
title: ID3D12GraphicsCommandList1::SetSamplePositions (d3d12.h)
description: This method configures the sample positions used by subsequent draw, copy, resolve, and similar operations.
helpviewer_keywords: ["ID3D12GraphicsCommandList1 interface","SetSamplePositions method","ID3D12GraphicsCommandList1.SetSamplePositions","ID3D12GraphicsCommandList1::SetSamplePositions","SetSamplePositions","SetSamplePositions method","SetSamplePositions method","ID3D12GraphicsCommandList1 interface","d3d12/ID3D12GraphicsCommandList1::SetSamplePositions","direct3d12.id3d12graphicscommandlist1_setsamplepositions"]
old-location: direct3d12\id3d12graphicscommandlist1_setsamplepositions.htm
tech.root: direct3d12
ms.assetid: 04627303-20C7-44B1-A62D-45003A13685B
ms.date: 08/10/2022
ms.keywords: ID3D12GraphicsCommandList1 interface,SetSamplePositions method, ID3D12GraphicsCommandList1.SetSamplePositions, ID3D12GraphicsCommandList1::SetSamplePositions, SetSamplePositions, SetSamplePositions method, SetSamplePositions method,ID3D12GraphicsCommandList1 interface, d3d12/ID3D12GraphicsCommandList1::SetSamplePositions, direct3d12.id3d12graphicscommandlist1_setsamplepositions
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
 - ID3D12GraphicsCommandList1::SetSamplePositions
 - d3d12/ID3D12GraphicsCommandList1::SetSamplePositions
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
 - ID3D12GraphicsCommandList1.SetSamplePositions
---

# ID3D12GraphicsCommandList1::SetSamplePositions


## -description

This method configures the sample positions used by subsequent draw, copy, resolve, and similar operations.

## -parameters

### -param NumSamplesPerPixel [in]

Type: <b>UINT</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

Specifies the number of samples to take, per pixel. This value can be 1, 2, 4, 8, or 16, otherwise the SetSamplePosition call is dropped. The number of samples must match the sample count configured in the PSO at draw time, otherwise the behavior is undefined.

### -param NumPixels [in]

Type: <b>UINT</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

Specifies the number of pixels that sample patterns are being specified for. This value can be either 1 or 4, otherwise the SetSamplePosition call is dropped. A value of 1 configures a single sample pattern to be used for each pixel; a value of 4 configures separate sample patterns for each pixel in a 2x2 pixel grid which is repeated over the render-target or viewport space, aligned to even coordinates.

Note that the maximum number of combined samples can't exceed 16, otherwise the call is dropped. If NumPixels is set to 4, NumSamplesPerPixel can specify no more than 4 samples.

### -param pSamplePositions [in]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sample_position">D3D12_SAMPLE_POSITION</a>*</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_reads_(NumSamplesPerPixel*NumPixels)</code>

Specifies an array of D3D12_SAMPLE_POSITION elements. The size of the array is NumPixels * NumSamplesPerPixel. If NumPixels is set to 4, then the first group of sample positions corresponds to the upper-left pixel in the 2x2 grid of pixels; the next group of sample positions corresponds to the upper-right pixel, the next group to the lower-left pixel, and the final group to the lower-right pixel.

If centroid interpolation is used during rendering, the order of positions for each pixel determines centroid-sampling priority. That is, the first covered sample in the order specified is chosen as the centroid sample location.

## -remarks

The operational semantics of sample positions are determined by the various draw, copy, resolve, and other operations that can occur.

<b>CommandList:</b> In the absence of any prior calls to SetSamplePositions in a CommandList, samples assume the default position based on the Pipeline State Object (PSO). The default positions are determined either by the SAMPLE_DESC portion of the PSO if it is present, or by the standard sample positions if the RASTERIZER_DESC portion of the PSO has ForcedSampleCount set to a value greater than 0.

After SetSamplePosition has been called, subsequent draw calls must use a PSO that specifies a matching sample count either using the SAMPLE_DESC portion of the PSO, or ForcedSampleCount in the RASTERIZER_DESC portion of the PSO.

SetSamplePositions can only be called on a graphics CommandList. It can't be called in a bundle; bundles inherit sample position state from the calling CommandList and don't modify it.

Calling SetSamplePositions(0, 0, NULL) reverts the sample positions to their default values.

<b>Clear RenderTarget:</b> Sample positions are ignored when clearing a render target.

<b>Clear DepthStencil:</b> When clearing the depth portion of a depth-stencil surface or any region of it, the sample positions must be set to match those of future rendering to the cleared surface or region; the contents of any uncleared regions produced using different sample positions become undefined.

When clearing the stencil portion of a depth-stencil surface or any region of it, the sample positions are ignored.

<b>Draw to RenderTarget:</b> When drawing to a render target the sample positions can be changed for each draw call, even when drawing to a region that overlaps previous draw calls. The current sample positions determine the operational semantics of each draw call and samples are taken from taken from the stored contents of the render target, even if the contents were produced using different sample positions.

<b>Draw using DepthStencil:</b> When drawing to a depth-stencil surface (read or write) or any region of it, the sample positions must be set to match those used to clear the affected region previously. To use a different sample position, the target region must be cleared first. The pixels outside the clear region are unaffected.

Hardware may store the depth portion or a depth-stencil surface as plane equations, and evaluate them to produce depth values when the application issues a read. Only the rasterizer and output-merger are required to support programmable sample positions of the depth portion of a depth-stencil surface. Any other read or write of the depth portion that has been rendered with sample positions set may ignore them and instead sample at the standard positions.

<b>Resolve RenderTarget:</b> When resolving a render target or any region of it, the sample positions are ignored; these APIs operate only on stored color values.

<b>Resolve DepthStencil:</b> When resolving the depth portion of a depth-stencil surface or any region of it, the sample positions must be set to match those of past rendering to the resolved surface or region. To use a different sample position, the target region must be cleared first.

When resolving the stencil portion of a depth-stencil surface or any region of it, the sample positions are ignored; stencil resolves operate only on stored stencil values.

<b>Copy RenderTarget:</b> When copying from a render target, the sample positions are ignored regardless of whether it is a full or partial copy.

<b>Copy DepthStencil (Full Subresource):</b> When copying a full subresource from a depth-stencil surface, the sample positions must be set to match the sample positions used to generate the source surface. To use a different sample position, the target region must be cleared first.

On some hardware properties of the source surface (such as stored plane equations for depth values) transfer to the destination. Therefore, if the destination surface is subsequently drawn to, the sample positions originally used to generate the source content need to be used with the destination surface. The API requires this on all hardware for consistency even if it may only apply to some.

<b>Copy DepthStencil (Partial Subresource):</b> When copying a partial subresource from a depth-stencil surface, the sample positions must be set to match the sample positions used to generate the source surface, similarly to copying a full subresource. However, if the content of an affected destination subresources is only partially covered by the copy, the contents of the uncovered portion within those subresources becomes undefined unless all of it was generated using the same sample positions as the copy source. To use a different sample position, the target region must be cleared first.

When copying a partial subresource from the stencil portion of a depth-stencil surface, the sample postions are ignored. It doesn’t matter what sample positions were used to generate content for any other areas of the destination buffer not covered by the copy – those contents remain valid.

<b>Shader SamplePos:</b> The HLSL SamplePos intrinsic is not aware of programmable sample positions and results returned to shaders calling this on a surface rendered with programmable positions is undefined. Applications must pass coordinates into their shader manually if needed. Similarly evaluating attributes by sample index is undefined with programmable sample positions.

<b>Transitioning out of DEPTH_READ or DEPTH_WRITE state:</b> If a subresource in DEPTH_READ or DEPTH_WRITE state is transitioned to any other state, including COPY_SOURCE or RESOLVE_SOURCE, some hardware might need to decompress the surface. Therefore, the sample positions must be set on the command list to match those used to generate the content in the source surface. Furthermore, for any subsequent transitions of the surface while the same depth data remains in it, the sample positions must continue to match those set on the command list. To use a different sample position, the target region must be cleared first.

If an application wants to minimize the decompressed area when only a portion needs to be used, or just to preserve compression, ResolveSubresourceRegion() can be called in DECOMPRESS mode with a rect specified.  This will decompress just the relevant area to a separate resource leaving the source intact on some hardware, though on other hardware even the source area is decompressed. The separate explicitly decompressed resource can then be transitioned to the desired state (such as SHADER_RESOURCE).

<b>Transitioning out of RENDER_TARGET state:</b> If a subresource in RENDER_TARGET state is transitioned to anything other than COPY_SOURCE or RESOLVE_SOURCE, some implementations may need to decompress the surface. This decompression is agnostic to sample positions.

If an application wants to minimize the decompressed area when only a portion needs to be used, or just to preserve compression, ResolveSubresourceRegion() can be called in DECOMPRESS mode with a rect specified.  This will decompress just the relevant area to a separate resource leaving the source intact on some hardware, though on other hardware even the source area is decompressed. The separate explicitly decompressed resource can then be transitioned to the desired state (such as SHADER_RESOURCE).

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist1">ID3D12GraphicsCommandList1</a>