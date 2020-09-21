---
UID: NS:d3d11shadertracing.D3D11_TRACE_STATS
title: D3D11_TRACE_STATS (d3d11shadertracing.h)
description: Specifies statistics about a trace.
helpviewer_keywords: ["D3D11_TRACE_STATS","D3D11_TRACE_STATS structure [Direct3D 11]","d3d11shadertracing/D3D11_TRACE_STATS","direct3d11.d3d11_trace_stats"]
old-location: direct3d11\d3d11_trace_stats.htm
tech.root: direct3d11
ms.assetid: E4E44F7F-3760-490D-9BA3-677F63B93AA6
ms.date: 12/05/2018
ms.keywords: D3D11_TRACE_STATS, D3D11_TRACE_STATS structure [Direct3D 11], d3d11shadertracing/D3D11_TRACE_STATS, direct3d11.d3d11_trace_stats
req.header: d3d11shadertracing.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: D3D11_TRACE_STATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TRACE_STATS
 - d3d11shadertracing/D3D11_TRACE_STATS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11ShaderTracing.h
api_name:
 - D3D11_TRACE_STATS
---

## -description

Specifies statistics about a trace.

## -struct-fields

### -field TraceDesc

A  <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_shader_trace_desc">D3D11_SHADER_TRACE_DESC</a> structure that describes the shader trace object for which this structure specifies statistics.

### -field NumInvocationsInStamp

The number of calls in the stamp for the trace. This value is always 1 for vertex shaders, hull shaders, domain shaders, geometry shaders, and compute shaders. This value is 4 for pixel shaders.

### -field TargetStampIndex

The index of the target stamp. This value is always 0 for vertex shaders, hull shaders, domain shaders, geometry shaders, and compute shaders. However, for pixel shaders this value indicates which of the four pixels in the stamp is the target for the trace.  You can examine the traces for other pixels in the stamp to determine how derivative calculations occurred. You can make this determination by correlating the registers across traces.

### -field NumTraceSteps

The total number of steps for the trace. This number is the same for all stamp calls.

### -field InputMask

The component trace mask for each input v# register. For information about D3D11_TRACE_COMPONENT_MASK, see <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_trace_value">D3D11_TRACE_VALUE</a>.

For vertex shaders, geometry shaders, pixel shaders, hull shaders, and domain shaders, the valid range is [0..31]. For compute shaders, this member is not applicable. Also, inputs for geometry shaders are 2D-indexed. For example, consider v[vertex][attribute]. In this example, the range of [attribute] is [0..31]. The [vertex] axis is the same size for all inputs, which are determined by the <b>GSInputPrimitive</b> member.

Similarly, inputs for hull shader and domain shader are 2D-indexed. For example, consider v[vertex][attribute]. In this example, the range of [attribute] is [0..15]. The [vertex] axis is the same size for all inputs.

### -field OutputMask

The component trace mask for each output o# register. For information about D3D11_TRACE_COMPONENT_MASK, see <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_trace_value">D3D11_TRACE_VALUE</a>.

For vertex shaders and geometry shaders, the valid range is [0..31]. For pixel shaders, the valid range is [0..7]. For compute shaders, this member is not applicable. For output control points for hull shaders, the registers are 2D-indexed. For example, consider ocp[vertex][attribute]. In this example, the range of [attribute] is [0..31]. The [vertex] axis is the same size for all inputs.

### -field NumTemps

The number of temps, that is, 4x32 bit r# registers that are declared.

### -field MaxIndexableTempIndex

The maximum index #+1 of all indexable temps x#[] that are declared. If they are declared sparsely (for example, x3[12] and x200[30] only), this value is 201 (200+1).

### -field IndexableTempSize

The number of temps for each indexable temp x#[numTemps]. You can only have temps up to the value in the <b>MaxIndexableTempIndex</b> member.

### -field ImmediateConstantBufferSize

The number of 4x32 bit values (if any) that are in the immediate constant buffer.

### -field PixelCoverageMask

<div class="alert"><b>Note</b>  This member is for pixel shaders only, [stampIndex].</div>
<div> </div>
A mask that indicates which MSAA samples are covered for each stamp. This coverage occurs before alpha-to-coverage, depth, and stencil operations are performed on the pixel. For non-MSAA, examine the least significant bit (LSB). This mask can be 0 for pixels that are only executed to support derivatives for neighboring pixels.

### -field PixelDiscardedMask

<div class="alert"><b>Note</b>  This member is for pixel shaders only, [stampIndex].</div>
<div> </div>
A mask that indicates discarded samples.  If the pixel shader runs at pixel-frequency, "discard" turns off all the samples. 	If all the samples are off, the following four mask members are also 0.

### -field PixelCoverageMaskAfterShader

<div class="alert"><b>Note</b>  This member is for pixel shaders only, [stampIndex].</div>
<div> </div>
A mask that indicates the MSAA samples that are covered. For non-MSAA, examine the LSB.

### -field PixelCoverageMaskAfterA2CSampleMask

<div class="alert"><b>Note</b>  This member is for pixel shaders only, [stampIndex].</div>
<div> </div>
A mask that indicates the MSAA samples that are covered after alpha-to-coverage+sampleMask, but before depth and stencil. For non-MSAA, examine the LSB.

### -field PixelCoverageMaskAfterA2CSampleMaskDepth

<div class="alert"><b>Note</b>  This member is for pixel shaders only, [stampIndex].</div>
<div> </div>
A mask that indicates the MSAA samples that are covered after alpha-to-coverage+sampleMask+depth, but before stencil. For non-MSAA, examine the LSB.

### -field PixelCoverageMaskAfterA2CSampleMaskDepthStencil

<div class="alert"><b>Note</b>  This member is for pixel shaders only, [stampIndex].</div>
<div> </div>
A mask that indicates the MSAA samples that are covered after alpha-to-coverage+sampleMask+depth+stencil. For non-MSAA, examine the LSB.

### -field PSOutputsDepth

A value that specifies whether this trace is for a pixel shader that outputs the oDepth register. TRUE indicates that the pixel shader outputs the oDepth register; otherwise, FALSE.

### -field PSOutputsMask

A value that specifies whether this trace is for a pixel shader that outputs the oMask register. TRUE indicates that the pixel shader outputs the oMask register; otherwise, FALSE.

### -field GSInputPrimitive

A <a href="/windows/desktop/api/d3d11shadertracing/ne-d3d11shadertracing-d3d11_trace_gs_input_primitive">D3D11_TRACE_GS_INPUT_PRIMITIVE</a>-typed value that identifies the type of geometry shader input primitive. That is, this value identifies:  {point, line, triangle, line_adj, triangle_adj} or the number of vertices: 1, 2, 3, 4, or 6 respectively. For example, for a line, input v[][#] is actually v[2][#]. For vertex shaders and pixel shaders, set this member to <a href="/windows/desktop/api/d3d11shadertracing/ne-d3d11shadertracing-d3d11_trace_gs_input_primitive">D3D11_TRACE_GS_INPUT_PRIMITIVE_UNDEFINED</a>.

### -field GSInputsPrimitiveID

A value that specifies whether this trace is for a geometry shader that inputs the PrimitiveID register. TRUE indicates that the geometry shader inputs the PrimitiveID register; otherwise, FALSE.

### -field HSOutputPatchConstantMask

<div class="alert"><b>Note</b>  This member is for hull shaders only.</div>
<div> </div>
The component trace mask for the hull-shader output. For information about D3D11_TRACE_COMPONENT_MASK, see <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_trace_value">D3D11_TRACE_VALUE</a>.

The <a href="/windows/desktop/api/d3d11shadertracing/ne-d3d11shadertracing-d3d11_trace_register_type">D3D11_TRACE_INPUT_PRIMITIVE_ID_REGISTER</a> value is available through a call to the <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents">ID3D11ShaderTrace::GetInitialRegisterContents</a> method.

### -field DSInputPatchConstantMask

<div class="alert"><b>Note</b>  This member is for domain shaders only.</div>
<div> </div>
The component trace mask for the domain-shader input. For information about D3D11_TRACE_COMPONENT_MASK, see <a href="/windows/desktop/api/d3d11shadertracing/ns-d3d11shadertracing-d3d11_trace_value">D3D11_TRACE_VALUE</a>.

The following values are available through a call to the <a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents">ID3D11ShaderTrace::GetInitialRegisterContents</a> method:

<ul>
<li><a href="/windows/desktop/api/d3d11shadertracing/ne-d3d11shadertracing-d3d11_trace_register_type">D3D11_TRACE_INPUT_PRIMITIVE_ID_REGISTER</a></li>
<li><a href="/windows/desktop/api/d3d11shadertracing/ne-d3d11shadertracing-d3d11_trace_register_type">D3D11_TRACE_INPUT_DOMAIN_POINT_REGISTER</a></li>
</ul>

## -remarks

This API requires the Windows Software Development Kit (SDK) for Windows 8.

## -see-also

<a href="/windows/desktop/api/d3d11shadertracing/nf-d3d11shadertracing-id3d11shadertrace-gettracestats">ID3D11ShaderTrace::GetTraceStats</a>

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>