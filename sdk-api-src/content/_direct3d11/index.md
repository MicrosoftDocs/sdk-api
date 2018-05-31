---
UID: TP:direct3d11
ms.assetid: b11d0120-422b-381b-b4ce-ba3e6eb45625
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Direct3D 11 Graphics



Overview of the Direct3D 11 Graphics technology.

To develop Direct3D 11 Graphics, you need these headers:

 * [d3d11.h](..\d3d11\index.md)
 * [d3d11_1.h](..\d3d11_1\index.md)
 * [d3d11_2.h](..\d3d11_2\index.md)
 * [d3d11_3.h](..\d3d11_3\index.md)
 * [d3d11_4.h](..\d3d11_4\index.md)
 * [d3d11sdklayers.h](..\d3d11sdklayers\index.md)
 * [d3d11shader.h](..\d3d11shader\index.md)
 * [d3d11shadertracing.h](..\d3d11shadertracing\index.md)
 * [d3dcsx.h](..\d3dcsx\index.md)

For the programming guide, see [Direct3D 11 Graphics](/windows/desktop/direct3d11).

## Functions

| Title   | Description   |
| ---- |:---- |
| [D3D11CalcSubresource function](..\d3d11\nf-d3d11-d3d11calcsubresource.md) | Calculates a subresource index for a texture. |
| [D3D11CreateDevice function](..\d3d11\nf-d3d11-d3d11createdevice.md) | Creates a device that represents the display adapter. |
| [D3D11CreateDeviceAndSwapChain function](..\d3d11\nf-d3d11-d3d11createdeviceandswapchain.md) | Creates a device that represents the display adapter and a swap chain used for rendering. |
| [D3DDisassemble11Trace function](..\d3d11shadertracing\nf-d3d11shadertracing-d3ddisassemble11trace.md) | Disassembles a section of compiled Microsoft High Level Shader Language (HLSL) code that is specified by shader trace steps. |
| [D3DX11CreateFFT function](..\d3dcsx\nf-d3dcsx-d3dx11createfft.md) | Creates an ID3DX11FFT COM interface object. |
| [D3DX11CreateFFT1DComplex function](..\d3dcsx\nf-d3dcsx-d3dx11createfft1dcomplex.md) | Creates an ID3DX11FFT COM interface object. |
| [D3DX11CreateFFT1DReal function](..\d3dcsx\nf-d3dcsx-d3dx11createfft1dreal.md) | Creates an ID3DX11FFT COM interface object. |
| [D3DX11CreateFFT2DComplex function](..\d3dcsx\nf-d3dcsx-d3dx11createfft2dcomplex.md) | Creates an ID3DX11FFT COM interface object. |
| [D3DX11CreateFFT2DReal function](..\d3dcsx\nf-d3dcsx-d3dx11createfft2dreal.md) | Creates an ID3DX11FFT COM interface object. |
| [D3DX11CreateFFT3DComplex function](..\d3dcsx\nf-d3dcsx-d3dx11createfft3dcomplex.md) | Creates an ID3DX11FFT COM interface object. |
| [D3DX11CreateFFT3DReal function](..\d3dcsx\nf-d3dcsx-d3dx11createfft3dreal.md) | Creates an ID3DX11FFT COM interface object. |
| [D3DX11CreateScan function](..\d3dcsx\nf-d3dcsx-d3dx11createscan.md) | Creates a scan context. |
| [D3DX11CreateSegmentedScan function](..\d3dcsx\nf-d3dcsx-d3dx11createsegmentedscan.md) | Creates a segmented scan context. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [CD3D11_BLEND_DESC structure](..\d3d11\ns-d3d11-cd3d11_blend_desc.md) | Represents a blend-state structure and provides convenience methods for creating blend-state structures. |
| [CD3D11_BLEND_DESC1 structure](..\d3d11_1\ns-d3d11_1-cd3d11_blend_desc1.md) | Describes the blend state that you use in a call to ID3D11Device1 |
| [CD3D11_BUFFER_DESC structure](..\d3d11\ns-d3d11-cd3d11_buffer_desc.md) | Represents a buffer and provides convenience methods for creating buffers. |
| [CD3D11_QUERY_DESC1 structure](..\d3d11_3\ns-d3d11_3-cd3d11_query_desc1.md) | Describes a query. |
| [CD3D11_RASTERIZER_DESC1 structure](..\d3d11_1\ns-d3d11_1-cd3d11_rasterizer_desc1.md) | Describes rasterizer state. |
| [CD3D11_RASTERIZER_DESC2 structure](..\d3d11_3\ns-d3d11_3-cd3d11_rasterizer_desc2.md) | Describes rasterizer state. |
| [CD3D11_RENDER_TARGET_VIEW_DESC1 structure](..\d3d11_3\ns-d3d11_3-cd3d11_render_target_view_desc1.md) | Describes the subresources from a resource that are accessible using a render-target view. |
| [CD3D11_SHADER_RESOURCE_VIEW_DESC1 structure](..\d3d11_3\ns-d3d11_3-cd3d11_shader_resource_view_desc1.md) | Describes a shader-resource view. |
| [CD3D11_TEXTURE2D_DESC1 structure](..\d3d11_3\ns-d3d11_3-cd3d11_texture2d_desc1.md) | Describes a 2D texture. |
| [CD3D11_TEXTURE3D_DESC1 structure](..\d3d11_3\ns-d3d11_3-cd3d11_texture3d_desc1.md) | Describes a 3D texture. |
| [CD3D11_UNORDERED_ACCESS_VIEW_DESC1 structure](..\d3d11_3\ns-d3d11_3-cd3d11_unordered_access_view_desc1.md) | Describes the subresources from a resource that are accessible using an unordered-access view. |
| [D3D11_BLEND_DESC structure](..\d3d11\ns-d3d11-d3d11_blend_desc.md) | Describes the blend state that you use in a call to ID3D11Device |
| [D3D11_BLEND_DESC1 structure](..\d3d11_1\ns-d3d11_1-d3d11_blend_desc1.md) | Describes the blend state that you use in a call to ID3D11Device1 |
| [D3D11_BOX structure](..\d3d11\ns-d3d11-d3d11_box.md) | Defines a 3D box. |
| [D3D11_BUFFEREX_SRV structure](..\d3d11\ns-d3d11-d3d11_bufferex_srv.md) | Describes the elements in a raw buffer resource to use in a shader-resource view. |
| [D3D11_BUFFER_DESC structure](..\d3d11\ns-d3d11-d3d11_buffer_desc.md) | Describes a buffer resource. |
| [D3D11_BUFFER_RTV structure](..\d3d11\ns-d3d11-d3d11_buffer_rtv.md) | Specifies the elements in a buffer resource to use in a render-target view. |
| [D3D11_BUFFER_SRV structure](..\d3d11\ns-d3d11-d3d11_buffer_srv.md) | Specifies the elements in a buffer resource to use in a shader-resource view. |
| [D3D11_BUFFER_UAV structure](..\d3d11\ns-d3d11-d3d11_buffer_uav.md) | Describes the elements in a buffer to use in a unordered-access view. |
| [D3D11_CLASS_INSTANCE_DESC structure](..\d3d11\ns-d3d11-d3d11_class_instance_desc.md) | Describes an HLSL class instance. |
| [D3D11_COMPUTE_SHADER_TRACE_DESC structure](..\d3d11shadertracing\ns-d3d11shadertracing-d3d11_compute_shader_trace_desc.md) | Describes an instance of a compute shader to trace. |
| [D3D11_COUNTER_DESC structure](..\d3d11\ns-d3d11-d3d11_counter_desc.md) | Describes a counter. |
| [D3D11_COUNTER_INFO structure](..\d3d11\ns-d3d11-d3d11_counter_info.md) | Information about the video card's performance counter capabilities. |
| [D3D11_DEPTH_STENCILOP_DESC structure](..\d3d11\ns-d3d11-d3d11_depth_stencilop_desc.md) | Stencil operations that can be performed based on the results of stencil test. |
| [D3D11_DEPTH_STENCIL_DESC structure](..\d3d11\ns-d3d11-d3d11_depth_stencil_desc.md) | Describes depth-stencil state. |
| [D3D11_DEPTH_STENCIL_VIEW_DESC structure](..\d3d11\ns-d3d11-d3d11_depth_stencil_view_desc.md) | Specifies the subresources of a texture that are accessible from a depth-stencil view. |
| [D3D11_DOMAIN_SHADER_TRACE_DESC structure](..\d3d11shadertracing\ns-d3d11shadertracing-d3d11_domain_shader_trace_desc.md) | Describes an instance of a domain shader to trace. |
| [D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS structure](..\d3d11\ns-d3d11-d3d11_draw_indexed_instanced_indirect_args.md) | Arguments for draw indexed instanced indirect. |
| [D3D11_DRAW_INSTANCED_INDIRECT_ARGS structure](..\d3d11\ns-d3d11-d3d11_draw_instanced_indirect_args.md) | Arguments for draw instanced indirect. |
| [D3D11_FEATURE_DATA_ARCHITECTURE_INFO structure](..\d3d11\ns-d3d11-d3d11_feature_data_architecture_info.md) | Describes information about Direct3D 11.1 adapter architecture. |
| [D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure](..\d3d11\ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options.md) | Describes compute shader and raw and structured buffer support in the current graphics driver. |
| [D3D11_FEATURE_DATA_D3D11_OPTIONS structure](..\d3d11\ns-d3d11-d3d11_feature_data_d3d11_options.md) | Describes Direct3D 11.1 feature options in the current graphics driver. |
| [D3D11_FEATURE_DATA_D3D11_OPTIONS1 structure](..\d3d11\ns-d3d11-d3d11_feature_data_d3d11_options1.md) | Describes Direct3D 11.2 feature options in the current graphics driver. |
| [D3D11_FEATURE_DATA_D3D11_OPTIONS2 structure](..\d3d11\ns-d3d11-d3d11_feature_data_d3d11_options2.md) | Describes Direct3D 11.3 feature options in the current graphics driver. |
| [D3D11_FEATURE_DATA_D3D11_OPTIONS3 structure](..\d3d11\ns-d3d11-d3d11_feature_data_d3d11_options3.md) | Describes Direct3D 11.3 feature options in the current graphics driver. |
| [D3D11_FEATURE_DATA_D3D11_OPTIONS4 structure](..\d3d11_4\ns-d3d11_4-d3d11_feature_data_d3d11_options4.md) | Describes Direct3D 11.4 feature options in the current graphics driver. |
| [D3D11_FEATURE_DATA_D3D9_OPTIONS structure](..\d3d11\ns-d3d11-d3d11_feature_data_d3d9_options.md) | Describes Direct3D 9 feature options in the current graphics driver. |
| [D3D11_FEATURE_DATA_D3D9_OPTIONS1 structure](..\d3d11\ns-d3d11-d3d11_feature_data_d3d9_options1.md) | Describes Direct3D 9 feature options in the current graphics driver. |
| [D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT structure](..\d3d11\ns-d3d11-d3d11_feature_data_d3d9_shadow_support.md) | Describes Direct3D 9 shadow support in the current graphics driver. |
| [D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT structure](..\d3d11\ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support.md) | Describes whether simple instancing is supported. |
| [D3D11_FEATURE_DATA_DOUBLES structure](..\d3d11\ns-d3d11-d3d11_feature_data_doubles.md) | Describes double data type support in the current graphics driver. |
| [D3D11_FEATURE_DATA_FORMAT_SUPPORT structure](..\d3d11\ns-d3d11-d3d11_feature_data_format_support.md) | Describes which resources are supported by the current graphics driver for a given format. |
| [D3D11_FEATURE_DATA_FORMAT_SUPPORT2 structure](..\d3d11\ns-d3d11-d3d11_feature_data_format_support2.md) | Describes which unordered resource options are supported by the current graphics driver for a given format. |
| [D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT structure](..\d3d11\ns-d3d11-d3d11_feature_data_gpu_virtual_address_support.md) | Describes feature data GPU virtual address support, including maximum address bits per resource and per process. |
| [D3D11_FEATURE_DATA_MARKER_SUPPORT structure](..\d3d11\ns-d3d11-d3d11_feature_data_marker_support.md) | Describes whether a GPU profiling technique is supported. |
| [D3D11_FEATURE_DATA_SHADER_CACHE structure](..\d3d11\ns-d3d11-d3d11_feature_data_shader_cache.md) | Describes the level of shader caching supported in the current graphics driver. |
| [D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT structure](..\d3d11\ns-d3d11-d3d11_feature_data_shader_min_precision_support.md) | Describes precision support options for shaders in the current graphics driver. |
| [D3D11_FEATURE_DATA_THREADING structure](..\d3d11\ns-d3d11-d3d11_feature_data_threading.md) | Describes the multi-threading features that are supported by the current graphics driver. |
| [D3D11_GEOMETRY_SHADER_TRACE_DESC structure](..\d3d11shadertracing\ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc.md) | Describes an instance of a geometry shader to trace. |
| [D3D11_HULL_SHADER_TRACE_DESC structure](..\d3d11shadertracing\ns-d3d11shadertracing-d3d11_hull_shader_trace_desc.md) | Describes an instance of a hull shader to trace. |
| [D3D11_INFO_QUEUE_FILTER structure](..\d3d11sdklayers\ns-d3d11sdklayers-d3d11_info_queue_filter.md) | Debug message filter; contains a lists of message types to allow or deny. |
| [D3D11_INFO_QUEUE_FILTER_DESC structure](..\d3d11sdklayers\ns-d3d11sdklayers-d3d11_info_queue_filter_desc.md) | Allow or deny certain types of messages to pass through a filter. |
| [D3D11_INPUT_ELEMENT_DESC structure](..\d3d11\ns-d3d11-d3d11_input_element_desc.md) | A description of a single element for the input-assembler stage. |
| [D3D11_MAPPED_SUBRESOURCE structure](..\d3d11\ns-d3d11-d3d11_mapped_subresource.md) | Provides access to subresource data. |
| [D3D11_MESSAGE structure](..\d3d11sdklayers\ns-d3d11sdklayers-d3d11_message.md) | A debug message in the Information Queue. |
| [D3D11_PACKED_MIP_DESC structure](..\d3d11_2\ns-d3d11_2-d3d11_packed_mip_desc.md) | Describes the tile structure of a tiled resource with mipmaps. |
| [D3D11_PIXEL_SHADER_TRACE_DESC structure](..\d3d11shadertracing\ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc.md) | Describes an instance of a pixel shader to trace. |
| [D3D11_QUERY_DATA_PIPELINE_STATISTICS structure](..\d3d11\ns-d3d11-d3d11_query_data_pipeline_statistics.md) | Query information about graphics-pipeline activity in between calls to ID3D11DeviceContext |
| [D3D11_QUERY_DATA_SO_STATISTICS structure](..\d3d11\ns-d3d11-d3d11_query_data_so_statistics.md) | Query information about the amount of data streamed out to the stream-output buffers in between ID3D11DeviceContext |
| [D3D11_QUERY_DATA_TIMESTAMP_DISJOINT structure](..\d3d11\ns-d3d11-d3d11_query_data_timestamp_disjoint.md) | Query information about the reliability of a timestamp query. |
| [D3D11_QUERY_DESC structure](..\d3d11\ns-d3d11-d3d11_query_desc.md) | Describes a query. |
| [D3D11_QUERY_DESC1 structure](..\d3d11_3\ns-d3d11_3-d3d11_query_desc1.md) | Describes a query. |
| [D3D11_RASTERIZER_DESC structure](..\d3d11\ns-d3d11-d3d11_rasterizer_desc.md) | Describes rasterizer state. |
| [D3D11_RASTERIZER_DESC1 structure](..\d3d11_1\ns-d3d11_1-d3d11_rasterizer_desc1.md) | Describes rasterizer state. |
| [D3D11_RASTERIZER_DESC2 structure](..\d3d11_3\ns-d3d11_3-d3d11_rasterizer_desc2.md) | Describes rasterizer state. |
| [D3D11_RENDER_TARGET_BLEND_DESC structure](..\d3d11\ns-d3d11-d3d11_render_target_blend_desc.md) | Describes the blend state for a render target. |
| [D3D11_RENDER_TARGET_BLEND_DESC1 structure](..\d3d11_1\ns-d3d11_1-d3d11_render_target_blend_desc1.md) | Describes the blend state for a render target. |
| [D3D11_RENDER_TARGET_VIEW_DESC structure](..\d3d11\ns-d3d11-d3d11_render_target_view_desc.md) | Specifies the subresources from a resource that are accessible using a render-target view. |
| [D3D11_RENDER_TARGET_VIEW_DESC1 structure](..\d3d11_3\ns-d3d11_3-d3d11_render_target_view_desc1.md) | Describes the subresources from a resource that are accessible using a render-target view. |
| [D3D11_SAMPLER_DESC structure](..\d3d11\ns-d3d11-d3d11_sampler_desc.md) | Describes a sampler state. |
| [D3D11_SHADER_RESOURCE_VIEW_DESC structure](..\d3d11\ns-d3d11-d3d11_shader_resource_view_desc.md) | Describes a shader-resource view. |
| [D3D11_SHADER_RESOURCE_VIEW_DESC1 structure](..\d3d11_3\ns-d3d11_3-d3d11_shader_resource_view_desc1.md) | Describes a shader-resource view. |
| [D3D11_SHADER_TRACE_DESC structure](..\d3d11shadertracing\ns-d3d11shadertracing-d3d11_shader_trace_desc.md) | Describes a shader-trace object. |
| [D3D11_SO_DECLARATION_ENTRY structure](..\d3d11\ns-d3d11-d3d11_so_declaration_entry.md) | Description of a vertex element in a vertex buffer in an output slot. |
| [D3D11_SUBRESOURCE_DATA structure](..\d3d11\ns-d3d11-d3d11_subresource_data.md) | Specifies data for initializing a subresource. |
| [D3D11_SUBRESOURCE_TILING structure](..\d3d11_2\ns-d3d11_2-d3d11_subresource_tiling.md) | Describes a tiled subresource volume. |
| [D3D11_TEX1D_ARRAY_DSV structure](..\d3d11\ns-d3d11-d3d11_tex1d_array_dsv.md) | Specifies the subresources from an array of 1D textures to use in a depth-stencil view. |
| [D3D11_TEX1D_ARRAY_RTV structure](..\d3d11\ns-d3d11-d3d11_tex1d_array_rtv.md) | Specifies the subresources from an array of 1D textures to use in a render-target view. |
| [D3D11_TEX1D_ARRAY_SRV structure](..\d3d11\ns-d3d11-d3d11_tex1d_array_srv.md) | Specifies the subresources from an array of 1D textures to use in a shader-resource view. |
| [D3D11_TEX1D_ARRAY_UAV structure](..\d3d11\ns-d3d11-d3d11_tex1d_array_uav.md) | Describes an array of unordered-access 1D texture resources. |
| [D3D11_TEX1D_DSV structure](..\d3d11\ns-d3d11-d3d11_tex1d_dsv.md) | Specifies the subresource from a 1D texture that is accessible to a depth-stencil view. |
| [D3D11_TEX1D_RTV structure](..\d3d11\ns-d3d11-d3d11_tex1d_rtv.md) | Specifies the subresource from a 1D texture to use in a render-target view. |
| [D3D11_TEX1D_SRV structure](..\d3d11\ns-d3d11-d3d11_tex1d_srv.md) | Specifies the subresource from a 1D texture to use in a shader-resource view. |
| [D3D11_TEX1D_UAV structure](..\d3d11\ns-d3d11-d3d11_tex1d_uav.md) | Describes a unordered-access 1D texture resource. |
| [D3D11_TEX2DMS_ARRAY_DSV structure](..\d3d11\ns-d3d11-d3d11_tex2dms_array_dsv.md) | Specifies the subresources from an array of multisampled 2D textures for a depth-stencil view. |
| [D3D11_TEX2DMS_ARRAY_RTV structure](..\d3d11\ns-d3d11-d3d11_tex2dms_array_rtv.md) | Specifies the subresources from a an array of multisampled 2D textures to use in a render-target view. |
| [D3D11_TEX2DMS_ARRAY_SRV structure](..\d3d11\ns-d3d11-d3d11_tex2dms_array_srv.md) | Specifies the subresources from an array of multisampled 2D textures to use in a shader-resource view. |
| [D3D11_TEX2DMS_DSV structure](..\d3d11\ns-d3d11-d3d11_tex2dms_dsv.md) | Specifies the subresource from a multisampled 2D texture that is accessible to a depth-stencil view. |
| [D3D11_TEX2DMS_RTV structure](..\d3d11\ns-d3d11-d3d11_tex2dms_rtv.md) | Specifies the subresource from a multisampled 2D texture to use in a render-target view. |
| [D3D11_TEX2DMS_SRV structure](..\d3d11\ns-d3d11-d3d11_tex2dms_srv.md) | Specifies the subresources from a multisampled 2D texture to use in a shader-resource view. |
| [D3D11_TEX2D_ARRAY_DSV structure](..\d3d11\ns-d3d11-d3d11_tex2d_array_dsv.md) | Specifies the subresources from an array 2D textures that are accessible to a depth-stencil view. |
| [D3D11_TEX2D_ARRAY_RTV structure](..\d3d11\ns-d3d11-d3d11_tex2d_array_rtv.md) | Specifies the subresources from an array of 2D textures to use in a render-target view. |
| [D3D11_TEX2D_ARRAY_RTV1 structure](..\d3d11_3\ns-d3d11_3-d3d11_tex2d_array_rtv1.md) | Describes the subresources from an array of 2D textures to use in a render-target view. |
| [D3D11_TEX2D_ARRAY_SRV structure](..\d3d11\ns-d3d11-d3d11_tex2d_array_srv.md) | Specifies the subresources from an array of 2D textures to use in a shader-resource view. |
| [D3D11_TEX2D_ARRAY_SRV1 structure](..\d3d11_3\ns-d3d11_3-d3d11_tex2d_array_srv1.md) | Describes the subresources from an array of 2D textures to use in a shader-resource view. |
| [D3D11_TEX2D_ARRAY_UAV structure](..\d3d11\ns-d3d11-d3d11_tex2d_array_uav.md) | Describes an array of unordered-access 2D texture resources. |
| [D3D11_TEX2D_ARRAY_UAV1 structure](..\d3d11_3\ns-d3d11_3-d3d11_tex2d_array_uav1.md) | Describes an array of unordered-access 2D texture resources. |
| [D3D11_TEX2D_DSV structure](..\d3d11\ns-d3d11-d3d11_tex2d_dsv.md) | Specifies the subresource from a 2D texture that is accessible to a depth-stencil view. |
| [D3D11_TEX2D_RTV structure](..\d3d11\ns-d3d11-d3d11_tex2d_rtv.md) | Specifies the subresource from a 2D texture to use in a render-target view. |
| [D3D11_TEX2D_RTV1 structure](..\d3d11_3\ns-d3d11_3-d3d11_tex2d_rtv1.md) | Describes the subresource from a 2D texture to use in a render-target view. |
| [D3D11_TEX2D_SRV structure](..\d3d11\ns-d3d11-d3d11_tex2d_srv.md) | Specifies the subresource from a 2D texture to use in a shader-resource view. |
| [D3D11_TEX2D_SRV1 structure](..\d3d11_3\ns-d3d11_3-d3d11_tex2d_srv1.md) | Describes the subresource from a 2D texture to use in a shader-resource view. |
| [D3D11_TEX2D_UAV structure](..\d3d11\ns-d3d11-d3d11_tex2d_uav.md) | Describes a unordered-access 2D texture resource. |
| [D3D11_TEX2D_UAV1 structure](..\d3d11_3\ns-d3d11_3-d3d11_tex2d_uav1.md) | Describes a unordered-access 2D texture resource. |
| [D3D11_TEX3D_RTV structure](..\d3d11\ns-d3d11-d3d11_tex3d_rtv.md) | Specifies the subresources from a 3D texture to use in a render-target view. |
| [D3D11_TEX3D_SRV structure](..\d3d11\ns-d3d11-d3d11_tex3d_srv.md) | Specifies the subresources from a 3D texture to use in a shader-resource view. |
| [D3D11_TEX3D_UAV structure](..\d3d11\ns-d3d11-d3d11_tex3d_uav.md) | Describes a unordered-access 3D texture resource. |
| [D3D11_TEXCUBE_ARRAY_SRV structure](..\d3d11\ns-d3d11-d3d11_texcube_array_srv.md) | Specifies the subresources from an array of cube textures to use in a shader-resource view. |
| [D3D11_TEXCUBE_SRV structure](..\d3d11\ns-d3d11-d3d11_texcube_srv.md) | Specifies the subresource from a cube texture to use in a shader-resource view. |
| [D3D11_TEXTURE1D_DESC structure](..\d3d11\ns-d3d11-d3d11_texture1d_desc.md) | Describes a 1D texture. |
| [D3D11_TEXTURE2D_DESC structure](..\d3d11\ns-d3d11-d3d11_texture2d_desc.md) | Describes a 2D texture. |
| [D3D11_TEXTURE2D_DESC1 structure](..\d3d11_3\ns-d3d11_3-d3d11_texture2d_desc1.md) | Describes a 2D texture. |
| [D3D11_TEXTURE3D_DESC structure](..\d3d11\ns-d3d11-d3d11_texture3d_desc.md) | Describes a 3D texture. |
| [D3D11_TEXTURE3D_DESC1 structure](..\d3d11_3\ns-d3d11_3-d3d11_texture3d_desc1.md) | Describes a 3D texture. |
| [D3D11_TILED_RESOURCE_COORDINATE structure](..\d3d11_2\ns-d3d11_2-d3d11_tiled_resource_coordinate.md) | Describes the coordinates of a tiled resource. |
| [D3D11_TILE_REGION_SIZE structure](..\d3d11_2\ns-d3d11_2-d3d11_tile_region_size.md) | Describes the size of a tiled region. |
| [D3D11_TILE_SHAPE structure](..\d3d11_2\ns-d3d11_2-d3d11_tile_shape.md) | Describes the shape of a tile by specifying its dimensions. |
| [D3D11_TRACE_REGISTER structure](..\d3d11shadertracing\ns-d3d11shadertracing-d3d11_trace_register.md) | Describes a trace register. |
| [D3D11_TRACE_STATS structure](..\d3d11shadertracing\ns-d3d11shadertracing-d3d11_trace_stats.md) | Specifies statistics about a trace. |
| [D3D11_TRACE_STEP structure](..\d3d11shadertracing\ns-d3d11shadertracing-d3d11_trace_step.md) | Describes a trace step, which is an instruction. |
| [D3D11_TRACE_VALUE structure](..\d3d11shadertracing\ns-d3d11shadertracing-d3d11_trace_value.md) | Describes a trace value. |
| [D3D11_UNORDERED_ACCESS_VIEW_DESC structure](..\d3d11\ns-d3d11-d3d11_unordered_access_view_desc.md) | Specifies the subresources from a resource that are accessible using an unordered-access view. |
| [D3D11_UNORDERED_ACCESS_VIEW_DESC1 structure](..\d3d11_3\ns-d3d11_3-d3d11_unordered_access_view_desc1.md) | Describes the subresources from a resource that are accessible using an unordered-access view. |
| [D3D11_VERTEX_SHADER_TRACE_DESC structure](..\d3d11shadertracing\ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc.md) | Describes an instance of a vertex shader to trace. |
| [D3D11_VIEWPORT structure](..\d3d11\ns-d3d11-d3d11_viewport.md) | Defines the dimensions of a viewport. |
| [D3DX11_FFT_BUFFER_INFO structure](..\d3dcsx\ns-d3dcsx-d3dx11_fft_buffer_info.md) | Describes buffer requirements for an FFT. |
| [D3DX11_FFT_DESC structure](..\d3dcsx\ns-d3dcsx-d3dx11_fft_desc.md) | Describes an FFT. |
| [_D3D11_FUNCTION_DESC structure](..\d3d11shader\ns-d3d11shader-_d3d11_function_desc.md) | Describes a function. |
| [_D3D11_LIBRARY_DESC structure](..\d3d11shader\ns-d3d11shader-_d3d11_library_desc.md) | Describes a library. |
| [_D3D11_PARAMETER_DESC structure](..\d3d11shader\ns-d3d11shader-_d3d11_parameter_desc.md) | Describes a function parameter. |
| [_D3D11_SHADER_BUFFER_DESC structure](..\d3d11shader\ns-d3d11shader-_d3d11_shader_buffer_desc.md) | Describes a shader constant-buffer. |
| [_D3D11_SHADER_DESC structure](..\d3d11shader\ns-d3d11shader-_d3d11_shader_desc.md) | Describes a shader. |
| [_D3D11_SHADER_INPUT_BIND_DESC structure](..\d3d11shader\ns-d3d11shader-_d3d11_shader_input_bind_desc.md) | Describes how a shader resource is bound to a shader input. |
| [_D3D11_SHADER_TYPE_DESC structure](..\d3d11shader\ns-d3d11shader-_d3d11_shader_type_desc.md) | Describes a shader-variable type. |
| [_D3D11_SHADER_VARIABLE_DESC structure](..\d3d11shader\ns-d3d11shader-_d3d11_shader_variable_desc.md) | Describes a shader variable. |
| [_D3D11_SIGNATURE_PARAMETER_DESC structure](..\d3d11shader\ns-d3d11shader-_d3d11_signature_parameter_desc.md) | Describes a shader signature. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG enumeration](..\d3d11_1\ne-d3d11_1-d3d11_1_create_device_context_state_flag.md) | Describes flags that are used to create a device context state object (ID3DDeviceContextState) with the ID3D11Device1 |
| [D3D11_ASYNC_GETDATA_FLAG enumeration](..\d3d11\ne-d3d11-d3d11_async_getdata_flag.md) | Optional flags that control the behavior of ID3D11DeviceContext |
| [D3D11_BIND_FLAG enumeration](..\d3d11\ne-d3d11-d3d11_bind_flag.md) | Identifies how to bind a resource to the pipeline. |
| [D3D11_BLEND enumeration](..\d3d11\ne-d3d11-d3d11_blend.md) | Blend factors, which modulate values for the pixel shader and render target. |
| [D3D11_BLEND_OP enumeration](..\d3d11\ne-d3d11-d3d11_blend_op.md) | RGB or alpha blending operation. |
| [D3D11_BUFFEREX_SRV_FLAG enumeration](..\d3d11\ne-d3d11-d3d11_bufferex_srv_flag.md) | Identifies how to view a buffer resource. |
| [D3D11_BUFFER_UAV_FLAG enumeration](..\d3d11\ne-d3d11-d3d11_buffer_uav_flag.md) | Identifies unordered-access view options for a buffer resource. |
| [D3D11_CHECK_MULTISAMPLE_QUALITY_LEVELS_FLAG enumeration](..\d3d11_2\ne-d3d11_2-d3d11_check_multisample_quality_levels_flag.md) | Identifies how to check multisample quality levels. |
| [D3D11_CLEAR_FLAG enumeration](..\d3d11\ne-d3d11-d3d11_clear_flag.md) | Specifies the parts of the depth stencil to clear. |
| [D3D11_COLOR_WRITE_ENABLE enumeration](..\d3d11\ne-d3d11-d3d11_color_write_enable.md) | Identify which components of each pixel of a render target are writable during blending. |
| [D3D11_COMPARISON_FUNC enumeration](..\d3d11\ne-d3d11-d3d11_comparison_func.md) | Comparison options. |
| [D3D11_CONSERVATIVE_RASTERIZATION_MODE enumeration](..\d3d11_3\ne-d3d11_3-d3d11_conservative_rasterization_mode.md) | Identifies whether conservative rasterization is on or off. |
| [D3D11_CONSERVATIVE_RASTERIZATION_TIER enumeration](..\d3d11\ne-d3d11-d3d11_conservative_rasterization_tier.md) | Specifies if the hardware and driver support conservative rasterization and at what tier level. |
| [D3D11_CONTEXT_TYPE enumeration](..\d3d11_3\ne-d3d11_3-d3d11_context_type.md) | Specifies the context in which a query occurs. |
| [D3D11_COPY_FLAGS enumeration](..\d3d11_1\ne-d3d11_1-d3d11_copy_flags.md) | Specifies how to handle the existing contents of a resource during a copy or update operation of a region within that resource. |
| [D3D11_COUNTER enumeration](..\d3d11\ne-d3d11-d3d11_counter.md) | Options for performance counters. |
| [D3D11_COUNTER_TYPE enumeration](..\d3d11\ne-d3d11-d3d11_counter_type.md) | Data type of a performance counter. |
| [D3D11_CPU_ACCESS_FLAG enumeration](..\d3d11\ne-d3d11-d3d11_cpu_access_flag.md) | Specifies the types of CPU access allowed for a resource. |
| [D3D11_CREATE_DEVICE_FLAG enumeration](..\d3d11\ne-d3d11-d3d11_create_device_flag.md) | Describes parameters that are used to create a device. |
| [D3D11_CULL_MODE enumeration](..\d3d11\ne-d3d11-d3d11_cull_mode.md) | Indicates triangles facing a particular direction are not drawn. |
| [D3D11_DEPTH_WRITE_MASK enumeration](..\d3d11\ne-d3d11-d3d11_depth_write_mask.md) | Identify the portion of a depth-stencil buffer for writing depth data. |
| [D3D11_DEVICE_CONTEXT_TYPE enumeration](..\d3d11\ne-d3d11-d3d11_device_context_type.md) | Device context options. |
| [D3D11_DSV_DIMENSION enumeration](..\d3d11\ne-d3d11-d3d11_dsv_dimension.md) | Specifies how to access a resource used in a depth-stencil view. |
| [D3D11_DSV_FLAG enumeration](..\d3d11\ne-d3d11-d3d11_dsv_flag.md) | Depth-stencil view options. |
| [D3D11_FEATURE enumeration](..\d3d11\ne-d3d11-d3d11_feature.md) | Direct3D 11 feature options. |
| [D3D11_FENCE_FLAG enumeration](..\d3d11_3\ne-d3d11_3-d3d11_fence_flag.md) | Specifies fence options. |
| [D3D11_FILL_MODE enumeration](..\d3d11\ne-d3d11-d3d11_fill_mode.md) | Determines the fill mode to use when rendering triangles. |
| [D3D11_FILTER enumeration](..\d3d11\ne-d3d11-d3d11_filter.md) | Filtering options during texture sampling. |
| [D3D11_FILTER_REDUCTION_TYPE enumeration](..\d3d11\ne-d3d11-d3d11_filter_reduction_type.md) | Specifies the type of sampler filter reduction. |
| [D3D11_FILTER_TYPE enumeration](..\d3d11\ne-d3d11-d3d11_filter_type.md) | Types of magnification or minification sampler filters. |
| [D3D11_FORMAT_SUPPORT enumeration](..\d3d11\ne-d3d11-d3d11_format_support.md) | Which resources are supported for a given format and given device (see ID3D11Device |
| [D3D11_FORMAT_SUPPORT2 enumeration](..\d3d11\ne-d3d11-d3d11_format_support2.md) | Unordered resource support options for a compute shader resource (see ID3D11Device |
| [D3D11_INPUT_CLASSIFICATION enumeration](..\d3d11\ne-d3d11-d3d11_input_classification.md) | Type of data contained in an input slot. |
| [D3D11_LOGIC_OP enumeration](..\d3d11_1\ne-d3d11_1-d3d11_logic_op.md) | Specifies logical operations to configure for a render target. |
| [D3D11_MAP enumeration](..\d3d11\ne-d3d11-d3d11_map.md) | Identifies a resource to be accessed for reading and writing by the CPU. Applications may combine one or more of these flags. |
| [D3D11_MAP_FLAG enumeration](..\d3d11\ne-d3d11-d3d11_map_flag.md) | Specifies how the CPU should respond when an application calls the ID3D11DeviceContext |
| [D3D11_MESSAGE_CATEGORY enumeration](..\d3d11sdklayers\ne-d3d11sdklayers-d3d11_message_category.md) | Categories of debug messages. |
| [D3D11_MESSAGE_ID enumeration](..\d3d11sdklayers\ne-d3d11sdklayers-d3d11_message_id.md) | Debug messages for setting up an info-queue filter (see D3D11_INFO_QUEUE_FILTER); use these messages to allow or deny message categories to pass through the storage and retrieval filters. |
| [D3D11_MESSAGE_SEVERITY enumeration](..\d3d11sdklayers\ne-d3d11sdklayers-d3d11_message_severity.md) | Debug message severity levels for an information queue. |
| [D3D11_QUERY enumeration](..\d3d11\ne-d3d11-d3d11_query.md) | Query types. |
| [D3D11_QUERY_MISC_FLAG enumeration](..\d3d11\ne-d3d11-d3d11_query_misc_flag.md) | Flags that describe miscellaneous query behavior. |
| [D3D11_RAISE_FLAG enumeration](..\d3d11\ne-d3d11-d3d11_raise_flag.md) | Option(s) for raising an error to a non-continuable exception. |
| [D3D11_RESOURCE_DIMENSION enumeration](..\d3d11\ne-d3d11-d3d11_resource_dimension.md) | Identifies the type of resource being used. |
| [D3D11_RESOURCE_MISC_FLAG enumeration](..\d3d11\ne-d3d11-d3d11_resource_misc_flag.md) | Identifies options for resources. |
| [D3D11_RLDO_FLAGS enumeration](..\d3d11sdklayers\ne-d3d11sdklayers-d3d11_rldo_flags.md) | Options for the amount of information to report about a device object's lifetime. |
| [D3D11_RTV_DIMENSION enumeration](..\d3d11\ne-d3d11-d3d11_rtv_dimension.md) | These flags identify the type of resource that will be viewed as a render target. |
| [D3D11_SHADER_CACHE_SUPPORT_FLAGS enumeration](..\d3d11\ne-d3d11-d3d11_shader_cache_support_flags.md) | Describes the level of support for shader caching in the current graphics driver. |
| [D3D11_SHADER_MIN_PRECISION_SUPPORT enumeration](..\d3d11\ne-d3d11-d3d11_shader_min_precision_support.md) | Values that specify minimum precision levels at shader stages. |
| [D3D11_SHADER_TRACKING_OPTION enumeration](..\d3d11sdklayers\ne-d3d11sdklayers-d3d11_shader_tracking_option.md) | Options that specify how to perform shader debug tracking. |
| [D3D11_SHADER_TRACKING_RESOURCE_TYPE enumeration](..\d3d11sdklayers\ne-d3d11sdklayers-d3d11_shader_tracking_resource_type.md) | Indicates which resource types to track. |
| [D3D11_SHADER_TYPE enumeration](..\d3d11shadertracing\ne-d3d11shadertracing-d3d11_shader_type.md) | Identifies a shader type for tracing. |
| [D3D11_SHADER_VERSION_TYPE enumeration](..\d3d11shader\ne-d3d11shader-d3d11_shader_version_type.md) | Indicates shader type. |
| [D3D11_STANDARD_MULTISAMPLE_QUALITY_LEVELS enumeration](..\d3d11\ne-d3d11-d3d11_standard_multisample_quality_levels.md) | Specifies a multi-sample pattern type. |
| [D3D11_STENCIL_OP enumeration](..\d3d11\ne-d3d11-d3d11_stencil_op.md) | The stencil operations that can be performed during depth-stencil testing. |
| [D3D11_TEXTURECUBE_FACE enumeration](..\d3d11\ne-d3d11-d3d11_texturecube_face.md) | The different faces of a cube texture. |
| [D3D11_TEXTURE_ADDRESS_MODE enumeration](..\d3d11\ne-d3d11-d3d11_texture_address_mode.md) | Identify a technique for resolving texture coordinates that are outside of the boundaries of a texture. |
| [D3D11_TEXTURE_LAYOUT enumeration](..\d3d11_3\ne-d3d11_3-d3d11_texture_layout.md) | Specifies texture layout options. |
| [D3D11_TILED_RESOURCES_TIER enumeration](..\d3d11\ne-d3d11-d3d11_tiled_resources_tier.md) | Indicates the tier level at which tiled resources are supported. |
| [D3D11_TILE_COPY_FLAG enumeration](..\d3d11_2\ne-d3d11_2-d3d11_tile_copy_flag.md) | Identifies how to copy a tile. |
| [D3D11_TILE_MAPPING_FLAG enumeration](..\d3d11_2\ne-d3d11_2-d3d11_tile_mapping_flag.md) | Identifies how to perform a tile-mapping operation. |
| [D3D11_TILE_RANGE_FLAG enumeration](..\d3d11_2\ne-d3d11_2-d3d11_tile_range_flag.md) | Specifies a range of tile mappings to use with ID3D11DeviceContext2 |
| [D3D11_TRACE_GS_INPUT_PRIMITIVE enumeration](..\d3d11shadertracing\ne-d3d11shadertracing-d3d11_trace_gs_input_primitive.md) | Identifies the type of geometry shader input primitive. |
| [D3D11_TRACE_REGISTER_TYPE enumeration](..\d3d11shadertracing\ne-d3d11shadertracing-d3d11_trace_register_type.md) | Identifies a type of trace register. |
| [D3D11_UAV_DIMENSION enumeration](..\d3d11\ne-d3d11-d3d11_uav_dimension.md) | Unordered-access view options. |
| [D3D11_USAGE enumeration](..\d3d11\ne-d3d11-d3d11_usage.md) | Identifies expected resource use during rendering. The usage directly reflects whether a resource is accessible by the CPU and/or the graphics processing unit (GPU). |
| [D3DX11_FFT_CREATE_FLAG enumeration](..\d3dcsx\ne-d3dcsx-d3dx11_fft_create_flag.md) | FFT creation flags. |
| [D3DX11_FFT_DATA_TYPE enumeration](..\d3dcsx\ne-d3dcsx-d3dx11_fft_data_type.md) | FFT data types. |
| [D3DX11_FFT_DIM_MASK enumeration](..\d3dcsx\ne-d3dcsx-d3dx11_fft_dim_mask.md) | Number of dimensions for FFT data. |
| [D3DX11_SCAN_DATA_TYPE enumeration](..\d3dcsx\ne-d3dcsx-d3dx11_scan_data_type.md) | Type for scan data. |
| [D3DX11_SCAN_DIRECTION enumeration](..\d3dcsx\ne-d3dcsx-d3dx11_scan_direction.md) | Direction to perform scan in. |
| [D3DX11_SCAN_OPCODE enumeration](..\d3dcsx\ne-d3dcsx-d3dx11_scan_opcode.md) | Scan opcodes. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [ID3D11Asynchronous interface](..\d3d11\nn-d3d11-id3d11asynchronous.md) | This interface encapsulates methods for retrieving data from the GPU asynchronously. |
| [ID3D11BlendState interface](..\d3d11\nn-d3d11-id3d11blendstate.md) | The blend-state interface holds a description for blending state that you can bind to the output-merger stage. |
| [ID3D11BlendState1 interface](..\d3d11_1\nn-d3d11_1-id3d11blendstate1.md) | The blend-state interface holds a description for blending state that you can bind to the output-merger stage. This blend-state interface supports logical operations as well as blending operations. |
| [ID3D11Buffer interface](..\d3d11\nn-d3d11-id3d11buffer.md) | A buffer interface accesses a buffer resource, which is unstructured memory. Buffers typically store vertex or index data. |
| [ID3D11ClassInstance interface](..\d3d11\nn-d3d11-id3d11classinstance.md) | This interface encapsulates an HLSL class. |
| [ID3D11ClassLinkage interface](..\d3d11\nn-d3d11-id3d11classlinkage.md) | This interface encapsulates an HLSL dynamic linkage. |
| [ID3D11CommandList interface](..\d3d11\nn-d3d11-id3d11commandlist.md) | The ID3D11CommandList interface encapsulates a list of graphics commands for play back. |
| [ID3D11ComputeShader interface](..\d3d11\nn-d3d11-id3d11computeshader.md) | A compute-shader interface manages an executable program (a compute shader) that controls the compute-shader stage. |
| [ID3D11Counter interface](..\d3d11\nn-d3d11-id3d11counter.md) | This interface encapsulates methods for measuring GPU performance. |
| [ID3D11Debug interface](..\d3d11sdklayers\nn-d3d11sdklayers-id3d11debug.md) | A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on. |
| [ID3D11DepthStencilState interface](..\d3d11\nn-d3d11-id3d11depthstencilstate.md) | The depth-stencil-state interface holds a description for depth-stencil state that you can bind to the output-merger stage. |
| [ID3D11DepthStencilView interface](..\d3d11\nn-d3d11-id3d11depthstencilview.md) | A depth-stencil-view interface accesses a texture resource during depth-stencil testing. |
| [ID3D11Device interface](..\d3d11\nn-d3d11-id3d11device.md) | The device interface represents a virtual adapter; it is used to create resources. |
| [ID3D11Device1 interface](..\d3d11_1\nn-d3d11_1-id3d11device1.md) | The device interface represents a virtual adapter; it is used to create resources. ID3D11Device1 adds new methods to those in ID3D11Device. |
| [ID3D11Device2 interface](..\d3d11_2\nn-d3d11_2-id3d11device2.md) | The device interface represents a virtual adapter; it is used to create resources. ID3D11Device2 adds new methods to those in ID3D11Device1. |
| [ID3D11Device3 interface](..\d3d11_3\nn-d3d11_3-id3d11device3.md) | The device interface represents a virtual adapter; it is used to create resources. ID3D11Device3 adds new methods to those in ID3D11Device2. |
| [ID3D11Device4 interface](..\d3d11_4\nn-d3d11_4-id3d11device4.md) | The device interface represents a virtual adapter; it is used to create resources. ID3D11Device4 adds new methods to those in ID3D11Device3, such as RegisterDeviceRemovedEvent and UnregisterDeviceRemoved. |
| [ID3D11Device5 interface](..\d3d11_4\nn-d3d11_4-id3d11device5.md) | The device interface represents a virtual adapter; it is used to create resources. ID3D11Device5 adds new methods to those in ID3D11Device4. |
| [ID3D11DeviceChild interface](..\d3d11\nn-d3d11-id3d11devicechild.md) | A device-child interface accesses data used by a device. |
| [ID3D11DeviceContext interface](..\d3d11\nn-d3d11-id3d11devicecontext.md) | The ID3D11DeviceContext interface represents a device context which generates rendering commands. |
| [ID3D11DeviceContext1 interface](..\d3d11_1\nn-d3d11_1-id3d11devicecontext1.md) | The device context interface represents a device context; it is used to render commands. ID3D11DeviceContext1 adds new methods to those in ID3D11DeviceContext. |
| [ID3D11DeviceContext2 interface](..\d3d11_2\nn-d3d11_2-id3d11devicecontext2.md) | The device context interface represents a device context; it is used to render commands. ID3D11DeviceContext2 adds new methods to those in ID3D11DeviceContext1. |
| [ID3D11DeviceContext3 interface](..\d3d11_3\nn-d3d11_3-id3d11devicecontext3.md) | The device context interface represents a device context; it is used to render commands. ID3D11DeviceContext3 adds new methods to those in ID3D11DeviceContext2. |
| [ID3D11DeviceContext4 interface](..\d3d11_3\nn-d3d11_3-id3d11devicecontext4.md) | The device context interface represents a device context; it is used to render commands. ID3D11DeviceContext4 adds new methods to those in ID3D11DeviceContext3. |
| [ID3D11DomainShader interface](..\d3d11\nn-d3d11-id3d11domainshader.md) | A domain-shader interface manages an executable program (a domain shader) that controls the domain-shader stage. |
| [ID3D11Fence interface](..\d3d11_3\nn-d3d11_3-id3d11fence.md) | Represents a fence, an object used for synchronization of the CPU and one or more GPUs. |
| [ID3D11FunctionLinkingGraph interface](..\d3d11shader\nn-d3d11shader-id3d11functionlinkinggraph.md) | A function-linking-graph interface is used for constructing shaders that consist of a sequence of precompiled function calls that pass values to each other. |
| [ID3D11FunctionParameterReflection interface](..\d3d11shader\nn-d3d11shader-id3d11functionparameterreflection.md) | A function-parameter-reflection interface accesses function-parameter info. |
| [ID3D11FunctionReflection interface](..\d3d11shader\nn-d3d11shader-id3d11functionreflection.md) | A function-reflection interface accesses function info. |
| [ID3D11GeometryShader interface](..\d3d11\nn-d3d11-id3d11geometryshader.md) | A geometry-shader interface manages an executable program (a geometry shader) that controls the geometry-shader stage. |
| [ID3D11HullShader interface](..\d3d11\nn-d3d11-id3d11hullshader.md) | A hull-shader interface manages an executable program (a hull shader) that controls the hull-shader stage. |
| [ID3D11InfoQueue interface](..\d3d11sdklayers\nn-d3d11sdklayers-id3d11infoqueue.md) | An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack. |
| [ID3D11InputLayout interface](..\d3d11\nn-d3d11-id3d11inputlayout.md) | An input-layout interface holds a definition of how to feed vertex data that is laid out in memory into the input-assembler stage of the graphics pipeline. |
| [ID3D11LibraryReflection interface](..\d3d11shader\nn-d3d11shader-id3d11libraryreflection.md) | A library-reflection interface accesses library info. |
| [ID3D11Linker interface](..\d3d11shader\nn-d3d11shader-id3d11linker.md) | A linker interface is used to link a shader module. |
| [ID3D11LinkingNode interface](..\d3d11shader\nn-d3d11shader-id3d11linkingnode.md) | A linking-node interface is used for shader linking. |
| [ID3D11Module interface](..\d3d11shader\nn-d3d11shader-id3d11module.md) | A module interface creates an instance of a module that is used for resource rebinding. |
| [ID3D11ModuleInstance interface](..\d3d11shader\nn-d3d11shader-id3d11moduleinstance.md) | A module-instance interface is used for resource rebinding. |
| [ID3D11Multithread interface](..\d3d11_4\nn-d3d11_4-id3d11multithread.md) | Provides threading protection for critical sections of a multi-threaded application. |
| [ID3D11PixelShader interface](..\d3d11\nn-d3d11-id3d11pixelshader.md) | A pixel-shader interface manages an executable program (a pixel shader) that controls the pixel-shader stage. |
| [ID3D11Predicate interface](..\d3d11\nn-d3d11-id3d11predicate.md) | A predicate interface determines whether geometry should be processed depending on the results of a previous draw call. |
| [ID3D11Query interface](..\d3d11\nn-d3d11-id3d11query.md) | A query interface queries information from the GPU. |
| [ID3D11Query1 interface](..\d3d11_3\nn-d3d11_3-id3d11query1.md) | Represents a query object for querying information from the graphics processing unit (GPU). |
| [ID3D11RasterizerState interface](..\d3d11\nn-d3d11-id3d11rasterizerstate.md) | The rasterizer-state interface holds a description for rasterizer state that you can bind to the rasterizer stage. |
| [ID3D11RasterizerState1 interface](..\d3d11_1\nn-d3d11_1-id3d11rasterizerstate1.md) | The rasterizer-state interface holds a description for rasterizer state that you can bind to the rasterizer stage. This rasterizer-state interface supports forced sample count. |
| [ID3D11RasterizerState2 interface](..\d3d11_3\nn-d3d11_3-id3d11rasterizerstate2.md) | The rasterizer-state interface holds a description for rasterizer state that you can bind to the rasterizer stage. This rasterizer-state interface supports forced sample count and conservative rasterization mode. |
| [ID3D11RefDefaultTrackingOptions interface](..\d3d11sdklayers\nn-d3d11sdklayers-id3d11refdefaulttrackingoptions.md) | The default tracking interface sets reference default tracking options. |
| [ID3D11RefTrackingOptions interface](..\d3d11sdklayers\nn-d3d11sdklayers-id3d11reftrackingoptions.md) | The tracking interface sets reference tracking options. |
| [ID3D11RenderTargetView interface](..\d3d11\nn-d3d11-id3d11rendertargetview.md) | A render-target-view interface identifies the render-target subresources that can be accessed during rendering. |
| [ID3D11RenderTargetView1 interface](..\d3d11_3\nn-d3d11_3-id3d11rendertargetview1.md) | A render-target-view interface represents the render-target subresources that can be accessed during rendering. |
| [ID3D11Resource interface](..\d3d11\nn-d3d11-id3d11resource.md) | A resource interface provides common actions on all resources. |
| [ID3D11SamplerState interface](..\d3d11\nn-d3d11-id3d11samplerstate.md) | The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the pipeline for reference by texture sample operations. |
| [ID3D11ShaderReflection interface](..\d3d11shader\nn-d3d11shader-id3d11shaderreflection.md) | A shader-reflection interface accesses shader information. |
| [ID3D11ShaderReflectionConstantBuffer interface](..\d3d11shader\nn-d3d11shader-id3d11shaderreflectionconstantbuffer.md) | This shader-reflection interface provides access to a constant buffer. |
| [ID3D11ShaderReflectionType interface](..\d3d11shader\nn-d3d11shader-id3d11shaderreflectiontype.md) | This shader-reflection interface provides access to variable type. |
| [ID3D11ShaderReflectionVariable interface](..\d3d11shader\nn-d3d11shader-id3d11shaderreflectionvariable.md) | This shader-reflection interface provides access to a variable. |
| [ID3D11ShaderResourceView interface](..\d3d11\nn-d3d11-id3d11shaderresourceview.md) | A shader-resource-view interface specifies the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, and a texture. |
| [ID3D11ShaderResourceView1 interface](..\d3d11_3\nn-d3d11_3-id3d11shaderresourceview1.md) | A shader-resource-view interface represents the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, and a texture. |
| [ID3D11ShaderTrace interface](..\d3d11shadertracing\nn-d3d11shadertracing-id3d11shadertrace.md) | An ID3D11ShaderTrace interface implements methods for obtaining traces of shader executions. |
| [ID3D11ShaderTraceFactory interface](..\d3d11shadertracing\nn-d3d11shadertracing-id3d11shadertracefactory.md) | An ID3D11ShaderTraceFactory interface implements a method for generating shader trace information objects. |
| [ID3D11SwitchToRef interface](..\d3d11sdklayers\nn-d3d11sdklayers-id3d11switchtoref.md) | ID3D11SwitchToRef interface |
| [ID3D11Texture1D interface](..\d3d11\nn-d3d11-id3d11texture1d.md) | A 1D texture interface accesses texel data, which is structured memory. |
| [ID3D11Texture2D interface](..\d3d11\nn-d3d11-id3d11texture2d.md) | A 2D texture interface manages texel data, which is structured memory. |
| [ID3D11Texture2D1 interface](..\d3d11_3\nn-d3d11_3-id3d11texture2d1.md) | A 2D texture interface represents texel data, which is structured memory. |
| [ID3D11Texture3D interface](..\d3d11\nn-d3d11-id3d11texture3d.md) | A 3D texture interface accesses texel data, which is structured memory. |
| [ID3D11Texture3D1 interface](..\d3d11_3\nn-d3d11_3-id3d11texture3d1.md) | A 3D texture interface represents texel data, which is structured memory. |
| [ID3D11TracingDevice interface](..\d3d11sdklayers\nn-d3d11sdklayers-id3d11tracingdevice.md) | The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution. |
| [ID3D11UnorderedAccessView interface](..\d3d11\nn-d3d11-id3d11unorderedaccessview.md) | A view interface specifies the parts of a resource the pipeline can access during rendering. |
| [ID3D11UnorderedAccessView1 interface](..\d3d11_3\nn-d3d11_3-id3d11unorderedaccessview1.md) | An unordered-access-view interface represents the parts of a resource the pipeline can access during rendering. |
| [ID3D11VertexShader interface](..\d3d11\nn-d3d11-id3d11vertexshader.md) | A vertex-shader interface manages an executable program (a vertex shader) that controls the vertex-shader stage. |
| [ID3D11View interface](..\d3d11\nn-d3d11-id3d11view.md) | A view interface specifies the parts of a resource the pipeline can access during rendering. |
| [ID3DDeviceContextState interface](..\d3d11_1\nn-d3d11_1-id3ddevicecontextstate.md) | The ID3DDeviceContextState interface represents a context state object, which holds state and behavior information about a Microsoft Direct3D device. |
| [ID3DUserDefinedAnnotation interface](..\d3d11_1\nn-d3d11_1-id3duserdefinedannotation.md) | The ID3DUserDefinedAnnotation interface enables an application to describe conceptual sections and markers within the application's code flow. |
| [ID3DX11FFT interface](..\d3dcsx\nn-d3dcsx-id3dx11fft.md) | Encapsulates forward and inverse FFTs. |
| [ID3DX11Scan interface](..\d3dcsx\nn-d3dcsx-id3dx11scan.md) | Scan context. |
| [ID3DX11SegmentedScan interface](..\d3dcsx\nn-d3dcsx-id3dx11segmentedscan.md) | Segmented scan context. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [ID3D11Asynchronous::GetDataSize](..\d3d11\nf-d3d11-id3d11asynchronous-getdatasize.md) | Get the size of the data (in bytes) that is output when calling ID3D11DeviceContext |
| [ID3D11BlendState1::GetDesc1](..\d3d11_1\nf-d3d11_1-id3d11blendstate1-getdesc1.md) | Gets the description for blending state that you used to create the blend-state object. |
| [ID3D11BlendState::GetDesc](..\d3d11\nf-d3d11-id3d11blendstate-getdesc.md) | Gets the description for blending state that you used to create the blend-state object. |
| [ID3D11Buffer::GetDesc](..\d3d11\nf-d3d11-id3d11buffer-getdesc.md) | Get the properties of a buffer resource. |
| [ID3D11ClassInstance::GetClassLinkage](..\d3d11\nf-d3d11-id3d11classinstance-getclasslinkage.md) | Gets the ID3D11ClassLinkage object associated with the current HLSL class. |
| [ID3D11ClassInstance::GetDesc](..\d3d11\nf-d3d11-id3d11classinstance-getdesc.md) | Gets a description of the current HLSL class. |
| [ID3D11ClassInstance::GetInstanceName](..\d3d11\nf-d3d11-id3d11classinstance-getinstancename.md) | Gets the instance name of the current HLSL class. |
| [ID3D11ClassInstance::GetTypeName](..\d3d11\nf-d3d11-id3d11classinstance-gettypename.md) | Gets the type of the current HLSL class. |
| [ID3D11ClassLinkage::CreateClassInstance](..\d3d11\nf-d3d11-id3d11classlinkage-createclassinstance.md) | Initializes a class-instance object that represents an HLSL class instance. |
| [ID3D11ClassLinkage::GetClassInstance](..\d3d11\nf-d3d11-id3d11classlinkage-getclassinstance.md) | Gets the class-instance object that represents the specified HLSL class. |
| [ID3D11CommandList::GetContextFlags](..\d3d11\nf-d3d11-id3d11commandlist-getcontextflags.md) | Gets the initialization flags associated with the deferred context that created the command list. |
| [ID3D11Counter::GetDesc](..\d3d11\nf-d3d11-id3d11counter-getdesc.md) | Get a counter description. |
| [ID3D11Debug::GetFeatureMask](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11debug-getfeaturemask.md) | Get a bitfield of flags that indicates which debug features are on or off. |
| [ID3D11Debug::GetPresentPerRenderOpDelay](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11debug-getpresentperrenderopdelay.md) | Get the number of milliseconds to sleep after IDXGISwapChain |
| [ID3D11Debug::GetSwapChain](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11debug-getswapchain.md) | Get the swap chain that the runtime will use for automatically calling IDXGISwapChain |
| [ID3D11Debug::ReportLiveDeviceObjects](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11debug-reportlivedeviceobjects.md) | Report information about a device object's lifetime. |
| [ID3D11Debug::SetFeatureMask](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11debug-setfeaturemask.md) | Set a bit field of flags that will turn debug features on and off. |
| [ID3D11Debug::SetPresentPerRenderOpDelay](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11debug-setpresentperrenderopdelay.md) | Set the number of milliseconds to sleep after IDXGISwapChain |
| [ID3D11Debug::SetSwapChain](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11debug-setswapchain.md) | Sets a swap chain that the runtime will use for automatically calling IDXGISwapChain |
| [ID3D11Debug::ValidateContextForDispatch](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11debug-validatecontextfordispatch.md) | Verifies whether the dispatch pipeline state is valid. |
| [ID3D11Debug::ValidateContext](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11debug-validatecontext.md) | Check to see if the draw pipeline state is valid. |
| [ID3D11DepthStencilState::GetDesc](..\d3d11\nf-d3d11-id3d11depthstencilstate-getdesc.md) | Gets the description for depth-stencil state that you used to create the depth-stencil-state object. |
| [ID3D11DepthStencilView::GetDesc](..\d3d11\nf-d3d11-id3d11depthstencilview-getdesc.md) | Get the depth-stencil view. |
| [ID3D11Device1::CreateBlendState1](..\d3d11_1\nf-d3d11_1-id3d11device1-createblendstate1.md) | Creates a blend-state object that encapsulates blend state for the output-merger stage and allows the configuration of logic operations. |
| [ID3D11Device1::CreateDeferredContext1](..\d3d11_1\nf-d3d11_1-id3d11device1-createdeferredcontext1.md) | Creates a deferred context, which can record command lists. |
| [ID3D11Device1::CreateDeviceContextState](..\d3d11_1\nf-d3d11_1-id3d11device1-createdevicecontextstate.md) | Creates a context state object that holds all Microsoft Direct3D state and some Direct3D behavior. |
| [ID3D11Device1::CreateRasterizerState1](..\d3d11_1\nf-d3d11_1-id3d11device1-createrasterizerstate1.md) | Creates a rasterizer state object that informs the rasterizer stage how to behave and forces the sample count while UAV rendering or rasterizing. |
| [ID3D11Device1::GetImmediateContext1](..\d3d11_1\nf-d3d11_1-id3d11device1-getimmediatecontext1.md) | Gets an immediate context, which can play back command lists. |
| [ID3D11Device1::OpenSharedResource1](..\d3d11_1\nf-d3d11_1-id3d11device1-opensharedresource1.md) | Gives a device access to a shared resource that is referenced by a handle and that was created on a different device. |
| [ID3D11Device1::OpenSharedResourceByName](..\d3d11_1\nf-d3d11_1-id3d11device1-opensharedresourcebyname.md) | Gives a device access to a shared resource that is referenced by name and that was created on a different device. |
| [ID3D11Device2::CheckMultisampleQualityLevels1](..\d3d11_2\nf-d3d11_2-id3d11device2-checkmultisamplequalitylevels1.md) | Get the number of quality levels available during multisampling. |
| [ID3D11Device2::CreateDeferredContext2](..\d3d11_2\nf-d3d11_2-id3d11device2-createdeferredcontext2.md) | Creates a deferred context, which can record command lists. |
| [ID3D11Device2::GetImmediateContext2](..\d3d11_2\nf-d3d11_2-id3d11device2-getimmediatecontext2.md) | Gets an immediate context, which can play back command lists. |
| [ID3D11Device2::GetResourceTiling](..\d3d11_2\nf-d3d11_2-id3d11device2-getresourcetiling.md) | Gets info about how a tiled resource is broken into tiles. |
| [ID3D11Device3::CreateDeferredContext3](..\d3d11_3\nf-d3d11_3-id3d11device3-createdeferredcontext3.md) | Creates a deferred context, which can record command lists. |
| [ID3D11Device3::CreateQuery1](..\d3d11_3\nf-d3d11_3-id3d11device3-createquery1.md) | Creates a query object for querying information from the graphics processing unit (GPU). |
| [ID3D11Device3::CreateRasterizerState2](..\d3d11_3\nf-d3d11_3-id3d11device3-createrasterizerstate2.md) | Creates a rasterizer state object that informs the rasterizer stage how to behave and forces the sample count while UAV rendering or rasterizing. |
| [ID3D11Device3::CreateRenderTargetView1](..\d3d11_3\nf-d3d11_3-id3d11device3-createrendertargetview1.md) | Creates a render-target view for accessing resource data. |
| [ID3D11Device3::CreateShaderResourceView1](..\d3d11_3\nf-d3d11_3-id3d11device3-createshaderresourceview1.md) | Creates a shader-resource view for accessing data in a resource. |
| [ID3D11Device3::CreateTexture2D1](..\d3d11_3\nf-d3d11_3-id3d11device3-createtexture2d1.md) | Creates a 2D texture. |
| [ID3D11Device3::CreateTexture3D1](..\d3d11_3\nf-d3d11_3-id3d11device3-createtexture3d1.md) | Creates a 3D texture. |
| [ID3D11Device3::CreateUnorderedAccessView1](..\d3d11_3\nf-d3d11_3-id3d11device3-createunorderedaccessview1.md) | Creates a view for accessing an unordered access resource. |
| [ID3D11Device3::GetImmediateContext3](..\d3d11_3\nf-d3d11_3-id3d11device3-getimmediatecontext3.md) | Gets an immediate context, which can play back command lists. |
| [ID3D11Device3::ReadFromSubresource](..\d3d11_3\nf-d3d11_3-id3d11device3-readfromsubresource.md) | Copies data from a D3D11_USAGE_DEFAULT texture which was mapped using ID3D11DeviceContext3 |
| [ID3D11Device3::WriteToSubresource](..\d3d11_3\nf-d3d11_3-id3d11device3-writetosubresource.md) | Copies data into a D3D11_USAGE_DEFAULT texture which was mapped using ID3D11DeviceContext3 |
| [ID3D11Device4::RegisterDeviceRemovedEvent](..\d3d11_4\nf-d3d11_4-id3d11device4-registerdeviceremovedevent.md) | Registers the &#0034;device removed&#0034; event and indicates when a Direct3D device has become removed for any reason, using an asynchronous notification mechanism. |
| [ID3D11Device4::UnregisterDeviceRemoved](..\d3d11_4\nf-d3d11_4-id3d11device4-unregisterdeviceremoved.md) | Unregisters the &#0034;device removed&#0034; event. |
| [ID3D11Device5::CreateFence](..\d3d11_4\nf-d3d11_4-id3d11device5-createfence.md) | Creates a fence object. |
| [ID3D11Device5::OpenSharedFence](..\d3d11_4\nf-d3d11_4-id3d11device5-opensharedfence.md) | Opens a handle for a shared fence by using HANDLE and REFIID. |
| [ID3D11Device::CheckCounterInfo](..\d3d11\nf-d3d11-id3d11device-checkcounterinfo.md) | Get a counter's information. |
| [ID3D11Device::CheckCounter](..\d3d11\nf-d3d11-id3d11device-checkcounter.md) | Get the type, name, units of measure, and a description of an existing counter. |
| [ID3D11Device::CheckFeatureSupport](..\d3d11\nf-d3d11-id3d11device-checkfeaturesupport.md) | Gets information about the features that are supported by the current graphics driver. |
| [ID3D11Device::CheckFormatSupport](..\d3d11\nf-d3d11-id3d11device-checkformatsupport.md) | Get the support of a given format on the installed video device. |
| [ID3D11Device::CheckMultisampleQualityLevels](..\d3d11\nf-d3d11-id3d11device-checkmultisamplequalitylevels.md) | Get the number of quality levels available during multisampling. |
| [ID3D11Device::CreateBlendState](..\d3d11\nf-d3d11-id3d11device-createblendstate.md) | Create a blend-state object that encapsules blend state for the output-merger stage. |
| [ID3D11Device::CreateBuffer](..\d3d11\nf-d3d11-id3d11device-createbuffer.md) | Creates a buffer (vertex buffer, index buffer, or shader-constant buffer). |
| [ID3D11Device::CreateClassLinkage](..\d3d11\nf-d3d11-id3d11device-createclasslinkage.md) | Creates class linkage libraries to enable dynamic shader linkage. |
| [ID3D11Device::CreateComputeShader](..\d3d11\nf-d3d11-id3d11device-createcomputeshader.md) | Create a compute shader. |
| [ID3D11Device::CreateCounter](..\d3d11\nf-d3d11-id3d11device-createcounter.md) | Create a counter object for measuring GPU performance. |
| [ID3D11Device::CreateDeferredContext](..\d3d11\nf-d3d11-id3d11device-createdeferredcontext.md) | Creates a deferred context, which can record command lists. |
| [ID3D11Device::CreateDepthStencilState](..\d3d11\nf-d3d11-id3d11device-createdepthstencilstate.md) | Create a depth-stencil state object that encapsulates depth-stencil test information for the output-merger stage. |
| [ID3D11Device::CreateDepthStencilView](..\d3d11\nf-d3d11-id3d11device-createdepthstencilview.md) | Create a depth-stencil view for accessing resource data. |
| [ID3D11Device::CreateDomainShader](..\d3d11\nf-d3d11-id3d11device-createdomainshader.md) | Create a domain shader . |
| [ID3D11Device::CreateGeometryShaderWithStreamOutput](..\d3d11\nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput.md) | Creates a geometry shader that can write to streaming output buffers. |
| [ID3D11Device::CreateGeometryShader](..\d3d11\nf-d3d11-id3d11device-creategeometryshader.md) | Create a geometry shader. |
| [ID3D11Device::CreateHullShader](..\d3d11\nf-d3d11-id3d11device-createhullshader.md) | Create a hull shader. |
| [ID3D11Device::CreateInputLayout](..\d3d11\nf-d3d11-id3d11device-createinputlayout.md) | Create an input-layout object to describe the input-buffer data for the input-assembler stage. |
| [ID3D11Device::CreatePixelShader](..\d3d11\nf-d3d11-id3d11device-createpixelshader.md) | Create a pixel shader. |
| [ID3D11Device::CreatePredicate](..\d3d11\nf-d3d11-id3d11device-createpredicate.md) | Creates a predicate. |
| [ID3D11Device::CreateQuery](..\d3d11\nf-d3d11-id3d11device-createquery.md) | This interface encapsulates methods for querying information from the GPU. |
| [ID3D11Device::CreateRasterizerState](..\d3d11\nf-d3d11-id3d11device-createrasterizerstate.md) | Create a rasterizer state object that tells the rasterizer stage how to behave. |
| [ID3D11Device::CreateRenderTargetView](..\d3d11\nf-d3d11-id3d11device-createrendertargetview.md) | Creates a render-target view for accessing resource data. |
| [ID3D11Device::CreateSamplerState](..\d3d11\nf-d3d11-id3d11device-createsamplerstate.md) | Create a sampler-state object that encapsulates sampling information for a texture. |
| [ID3D11Device::CreateShaderResourceView](..\d3d11\nf-d3d11-id3d11device-createshaderresourceview.md) | Create a shader-resource view for accessing data in a resource. |
| [ID3D11Device::CreateTexture1D](..\d3d11\nf-d3d11-id3d11device-createtexture1d.md) | Creates an array of 1D textures. |
| [ID3D11Device::CreateTexture2D](..\d3d11\nf-d3d11-id3d11device-createtexture2d.md) | Create an array of 2D textures. |
| [ID3D11Device::CreateTexture3D](..\d3d11\nf-d3d11-id3d11device-createtexture3d.md) | Create a single 3D texture. |
| [ID3D11Device::CreateUnorderedAccessView](..\d3d11\nf-d3d11-id3d11device-createunorderedaccessview.md) | Creates a view for accessing an unordered access resource. |
| [ID3D11Device::CreateVertexShader](..\d3d11\nf-d3d11-id3d11device-createvertexshader.md) | Create a vertex-shader object from a compiled shader. |
| [ID3D11Device::GetCreationFlags](..\d3d11\nf-d3d11-id3d11device-getcreationflags.md) | Get the flags used during the call to create the device with D3D11CreateDevice. |
| [ID3D11Device::GetDeviceRemovedReason](..\d3d11\nf-d3d11-id3d11device-getdeviceremovedreason.md) | Get the reason why the device was removed. |
| [ID3D11Device::GetExceptionMode](..\d3d11\nf-d3d11-id3d11device-getexceptionmode.md) | Get the exception-mode flags. |
| [ID3D11Device::GetFeatureLevel](..\d3d11\nf-d3d11-id3d11device-getfeaturelevel.md) | Gets the feature level of the hardware device. |
| [ID3D11Device::GetImmediateContext](..\d3d11\nf-d3d11-id3d11device-getimmediatecontext.md) | Gets an immediate context, which can play back command lists. |
| [ID3D11Device::GetPrivateData](..\d3d11\nf-d3d11-id3d11device-getprivatedata.md) | Get application-defined data from a device. |
| [ID3D11Device::OpenSharedResource](..\d3d11\nf-d3d11-id3d11device-opensharedresource.md) | Give a device access to a shared resource created on a different device. |
| [ID3D11Device::SetExceptionMode](..\d3d11\nf-d3d11-id3d11device-setexceptionmode.md) | Get the exception-mode flags. |
| [ID3D11Device::SetPrivateDataInterface](..\d3d11\nf-d3d11-id3d11device-setprivatedatainterface.md) | Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid. |
| [ID3D11Device::SetPrivateData](..\d3d11\nf-d3d11-id3d11device-setprivatedata.md) | Set data to a device and associate that data with a guid. |
| [ID3D11DeviceChild::GetDevice](..\d3d11\nf-d3d11-id3d11devicechild-getdevice.md) | Get a pointer to the device that created this interface. |
| [ID3D11DeviceChild::GetPrivateData](..\d3d11\nf-d3d11-id3d11devicechild-getprivatedata.md) | Get application-defined data from a device child. |
| [ID3D11DeviceChild::SetPrivateDataInterface](..\d3d11\nf-d3d11-id3d11devicechild-setprivatedatainterface.md) | Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid. |
| [ID3D11DeviceChild::SetPrivateData](..\d3d11\nf-d3d11-id3d11devicechild-setprivatedata.md) | Set application-defined data to a device child and associate that data with an application-defined guid. |
| [ID3D11DeviceContext1::CSGetConstantBuffers1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-csgetconstantbuffers1.md) | Gets the constant buffers that the compute-shader stage uses. |
| [ID3D11DeviceContext1::CSSetConstantBuffers1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1.md) | Sets the constant buffers that the compute-shader stage uses. |
| [ID3D11DeviceContext1::ClearView](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-clearview.md) | Sets all the elements in a resource view to one value. |
| [ID3D11DeviceContext1::CopySubresourceRegion1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1.md) | Copies a region from a source resource to a destination resource. |
| [ID3D11DeviceContext1::DSGetConstantBuffers1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-dsgetconstantbuffers1.md) | Gets the constant buffers that the domain-shader stage uses. |
| [ID3D11DeviceContext1::DSSetConstantBuffers1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1.md) | Sets the constant buffers that the domain-shader stage uses. |
| [ID3D11DeviceContext1::DiscardResource](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-discardresource.md) | Discards a resource from the device context. |
| [ID3D11DeviceContext1::DiscardView1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-discardview1.md) | Discards the specified elements in a resource view from the device context. |
| [ID3D11DeviceContext1::DiscardView](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-discardview.md) | Discards a resource view from the device context. |
| [ID3D11DeviceContext1::GSGetConstantBuffers1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-gsgetconstantbuffers1.md) | Gets the constant buffers that the geometry shader pipeline stage uses. |
| [ID3D11DeviceContext1::GSSetConstantBuffers1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-gssetconstantbuffers1.md) | Sets the constant buffers that the geometry shader pipeline stage uses. |
| [ID3D11DeviceContext1::HSGetConstantBuffers1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-hsgetconstantbuffers1.md) | Gets the constant buffers that the hull-shader stage uses. |
| [ID3D11DeviceContext1::HSSetConstantBuffers1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-hssetconstantbuffers1.md) | Sets the constant buffers that the hull-shader stage of the pipeline uses. |
| [ID3D11DeviceContext1::PSGetConstantBuffers1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-psgetconstantbuffers1.md) | Gets the constant buffers that the pixel shader pipeline stage uses. |
| [ID3D11DeviceContext1::PSSetConstantBuffers1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1.md) | Sets the constant buffers that the pixel shader pipeline stage uses, and enables the shader to access other parts of the buffer. |
| [ID3D11DeviceContext1::SwapDeviceContextState](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate.md) | Activates the given context state object and changes the current device behavior to Direct3D 11, Direct3D 10.1, or Direct3D 10. |
| [ID3D11DeviceContext1::UpdateSubresource1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-updatesubresource1.md) | The CPU copies data from memory to a subresource created in non-mappable memory. |
| [ID3D11DeviceContext1::VSGetConstantBuffers1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-vsgetconstantbuffers1.md) | Gets the constant buffers that the vertex shader pipeline stage uses. |
| [ID3D11DeviceContext1::VSSetConstantBuffers1](..\d3d11_1\nf-d3d11_1-id3d11devicecontext1-vssetconstantbuffers1.md) | Sets the constant buffers that the vertex shader pipeline stage uses. |
| [ID3D11DeviceContext2::BeginEventInt](..\d3d11_2\nf-d3d11_2-id3d11devicecontext2-begineventint.md) | Allows applications to annotate the beginning of a range of graphics commands. |
| [ID3D11DeviceContext2::CopyTileMappings](..\d3d11_2\nf-d3d11_2-id3d11devicecontext2-copytilemappings.md) | Copies mappings from a source tiled resource to a destination tiled resource. |
| [ID3D11DeviceContext2::CopyTiles](..\d3d11_2\nf-d3d11_2-id3d11devicecontext2-copytiles.md) | Copies tiles from buffer to tiled resource or vice versa. |
| [ID3D11DeviceContext2::EndEvent](..\d3d11_2\nf-d3d11_2-id3d11devicecontext2-endevent.md) | Allows applications to annotate the end of a range of graphics commands. |
| [ID3D11DeviceContext2::IsAnnotationEnabled](..\d3d11_2\nf-d3d11_2-id3d11devicecontext2-isannotationenabled.md) | Allows apps to determine when either a capture or profiling request is enabled. |
| [ID3D11DeviceContext2::ResizeTilePool](..\d3d11_2\nf-d3d11_2-id3d11devicecontext2-resizetilepool.md) | Resizes a tile pool. |
| [ID3D11DeviceContext2::SetMarkerInt](..\d3d11_2\nf-d3d11_2-id3d11devicecontext2-setmarkerint.md) | Allows applications to annotate graphics commands. |
| [ID3D11DeviceContext2::TiledResourceBarrier](..\d3d11_2\nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier.md) | Specifies a data access ordering constraint between multiple tiled resources. |
| [ID3D11DeviceContext2::UpdateTileMappings](..\d3d11_2\nf-d3d11_2-id3d11devicecontext2-updatetilemappings.md) | Updates mappings of tile locations in tiled resources to memory locations in a tile pool. |
| [ID3D11DeviceContext2::UpdateTiles](..\d3d11_2\nf-d3d11_2-id3d11devicecontext2-updatetiles.md) | Updates tiles by copying from app memory to the tiled resource. |
| [ID3D11DeviceContext3::Flush1](..\d3d11_3\nf-d3d11_3-id3d11devicecontext3-flush1.md) | Sends queued-up commands in the command buffer to the graphics processing unit (GPU), with a specified context type and an optional event handle to create an event query. |
| [ID3D11DeviceContext3::GetHardwareProtectionState](..\d3d11_3\nf-d3d11_3-id3d11devicecontext3-gethardwareprotectionstate.md) | Gets whether hardware protection is enabled. |
| [ID3D11DeviceContext3::SetHardwareProtectionState](..\d3d11_3\nf-d3d11_3-id3d11devicecontext3-sethardwareprotectionstate.md) | Sets the hardware protection state. |
| [ID3D11DeviceContext4::Signal](..\d3d11_3\nf-d3d11_3-id3d11devicecontext4-signal.md) | Updates a fence to a specified value after all previous work has completed. |
| [ID3D11DeviceContext4::Wait](..\d3d11_3\nf-d3d11_3-id3d11devicecontext4-wait.md) | Waits until the specified fence reaches or exceeds the specified value before future work can begin. |
| [ID3D11DeviceContext::Begin](..\d3d11\nf-d3d11-id3d11devicecontext-begin.md) | Mark the beginning of a series of commands. |
| [ID3D11DeviceContext::CSGetConstantBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-csgetconstantbuffers.md) | Get the constant buffers used by the compute-shader stage. |
| [ID3D11DeviceContext::CSGetSamplers](..\d3d11\nf-d3d11-id3d11devicecontext-csgetsamplers.md) | Get an array of sampler state interfaces from the compute-shader stage. |
| [ID3D11DeviceContext::CSGetShaderResources](..\d3d11\nf-d3d11-id3d11devicecontext-csgetshaderresources.md) | Get the compute-shader resources. |
| [ID3D11DeviceContext::CSGetShader](..\d3d11\nf-d3d11-id3d11devicecontext-csgetshader.md) | Get the compute shader currently set on the device. |
| [ID3D11DeviceContext::CSGetUnorderedAccessViews](..\d3d11\nf-d3d11-id3d11devicecontext-csgetunorderedaccessviews.md) | Gets an array of views for an unordered resource. |
| [ID3D11DeviceContext::CSSetConstantBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-cssetconstantbuffers.md) | Sets the constant buffers used by the compute-shader stage. |
| [ID3D11DeviceContext::CSSetSamplers](..\d3d11\nf-d3d11-id3d11devicecontext-cssetsamplers.md) | Set an array of sampler states to the compute-shader stage. |
| [ID3D11DeviceContext::CSSetShaderResources](..\d3d11\nf-d3d11-id3d11devicecontext-cssetshaderresources.md) | Bind an array of shader resources to the compute-shader stage. |
| [ID3D11DeviceContext::CSSetShader](..\d3d11\nf-d3d11-id3d11devicecontext-cssetshader.md) | Set a compute shader to the device. |
| [ID3D11DeviceContext::CSSetUnorderedAccessViews](..\d3d11\nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews.md) | Sets an array of views for an unordered resource. |
| [ID3D11DeviceContext::ClearDepthStencilView](..\d3d11\nf-d3d11-id3d11devicecontext-cleardepthstencilview.md) | Clears the depth-stencil resource. |
| [ID3D11DeviceContext::ClearRenderTargetView](..\d3d11\nf-d3d11-id3d11devicecontext-clearrendertargetview.md) | Set all the elements in a render target to one value. |
| [ID3D11DeviceContext::ClearState](..\d3d11\nf-d3d11-id3d11devicecontext-clearstate.md) | Restore all default settings. |
| [ID3D11DeviceContext::ClearUnorderedAccessViewFloat](..\d3d11\nf-d3d11-id3d11devicecontext-clearunorderedaccessviewfloat.md) | Clears an unordered access resource with a float value. |
| [ID3D11DeviceContext::ClearUnorderedAccessViewUint](..\d3d11\nf-d3d11-id3d11devicecontext-clearunorderedaccessviewuint.md) | Clears an unordered access resource with bit-precise values. |
| [ID3D11DeviceContext::CopyResource](..\d3d11\nf-d3d11-id3d11devicecontext-copyresource.md) | Copy the entire contents of the source resource to the destination resource using the GPU. |
| [ID3D11DeviceContext::CopyStructureCount](..\d3d11\nf-d3d11-id3d11devicecontext-copystructurecount.md) | Copies data from a buffer holding variable length data. |
| [ID3D11DeviceContext::CopySubresourceRegion](..\d3d11\nf-d3d11-id3d11devicecontext-copysubresourceregion.md) | Copy a region from a source resource to a destination resource. |
| [ID3D11DeviceContext::DSGetConstantBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-dsgetconstantbuffers.md) | Get the constant buffers used by the domain-shader stage. |
| [ID3D11DeviceContext::DSGetSamplers](..\d3d11\nf-d3d11-id3d11devicecontext-dsgetsamplers.md) | Get an array of sampler state interfaces from the domain-shader stage. |
| [ID3D11DeviceContext::DSGetShaderResources](..\d3d11\nf-d3d11-id3d11devicecontext-dsgetshaderresources.md) | Get the domain-shader resources. |
| [ID3D11DeviceContext::DSGetShader](..\d3d11\nf-d3d11-id3d11devicecontext-dsgetshader.md) | Get the domain shader currently set on the device. |
| [ID3D11DeviceContext::DSSetConstantBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-dssetconstantbuffers.md) | Sets the constant buffers used by the domain-shader stage. |
| [ID3D11DeviceContext::DSSetSamplers](..\d3d11\nf-d3d11-id3d11devicecontext-dssetsamplers.md) | Set an array of sampler states to the domain-shader stage. |
| [ID3D11DeviceContext::DSSetShaderResources](..\d3d11\nf-d3d11-id3d11devicecontext-dssetshaderresources.md) | Bind an array of shader resources to the domain-shader stage. |
| [ID3D11DeviceContext::DSSetShader](..\d3d11\nf-d3d11-id3d11devicecontext-dssetshader.md) | Set a domain shader to the device. |
| [ID3D11DeviceContext::DispatchIndirect](..\d3d11\nf-d3d11-id3d11devicecontext-dispatchindirect.md) | Execute a command list over one or more thread groups. |
| [ID3D11DeviceContext::Dispatch](..\d3d11\nf-d3d11-id3d11devicecontext-dispatch.md) | Execute a command list from a thread group. |
| [ID3D11DeviceContext::DrawAuto](..\d3d11\nf-d3d11-id3d11devicecontext-drawauto.md) | Draw geometry of an unknown size. |
| [ID3D11DeviceContext::DrawIndexedInstancedIndirect](..\d3d11\nf-d3d11-id3d11devicecontext-drawindexedinstancedindirect.md) | Draw indexed, instanced, GPU-generated primitives. |
| [ID3D11DeviceContext::DrawIndexedInstanced](..\d3d11\nf-d3d11-id3d11devicecontext-drawindexedinstanced.md) | Draw indexed, instanced primitives. |
| [ID3D11DeviceContext::DrawIndexed](..\d3d11\nf-d3d11-id3d11devicecontext-drawindexed.md) | Draw indexed, non-instanced primitives. |
| [ID3D11DeviceContext::DrawInstancedIndirect](..\d3d11\nf-d3d11-id3d11devicecontext-drawinstancedindirect.md) | Draw instanced, GPU-generated primitives. |
| [ID3D11DeviceContext::DrawInstanced](..\d3d11\nf-d3d11-id3d11devicecontext-drawinstanced.md) | Draw non-indexed, instanced primitives. |
| [ID3D11DeviceContext::Draw](..\d3d11\nf-d3d11-id3d11devicecontext-draw.md) | Draw non-indexed, non-instanced primitives. |
| [ID3D11DeviceContext::End](..\d3d11\nf-d3d11-id3d11devicecontext-end.md) | Mark the end of a series of commands. |
| [ID3D11DeviceContext::ExecuteCommandList](..\d3d11\nf-d3d11-id3d11devicecontext-executecommandlist.md) | Queues commands from a command list onto a device. |
| [ID3D11DeviceContext::FinishCommandList](..\d3d11\nf-d3d11-id3d11devicecontext-finishcommandlist.md) | Create a command list and record graphics commands into it. |
| [ID3D11DeviceContext::Flush](..\d3d11\nf-d3d11-id3d11devicecontext-flush.md) | Sends queued-up commands in the command buffer to the graphics processing unit (GPU). |
| [ID3D11DeviceContext::GSGetConstantBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-gsgetconstantbuffers.md) | Get the constant buffers used by the geometry shader pipeline stage. |
| [ID3D11DeviceContext::GSGetSamplers](..\d3d11\nf-d3d11-id3d11devicecontext-gsgetsamplers.md) | Get an array of sampler state interfaces from the geometry shader pipeline stage. |
| [ID3D11DeviceContext::GSGetShaderResources](..\d3d11\nf-d3d11-id3d11devicecontext-gsgetshaderresources.md) | Get the geometry shader resources. |
| [ID3D11DeviceContext::GSGetShader](..\d3d11\nf-d3d11-id3d11devicecontext-gsgetshader.md) | Get the geometry shader currently set on the device. |
| [ID3D11DeviceContext::GSSetConstantBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-gssetconstantbuffers.md) | Sets the constant buffers used by the geometry shader pipeline stage. |
| [ID3D11DeviceContext::GSSetSamplers](..\d3d11\nf-d3d11-id3d11devicecontext-gssetsamplers.md) | Set an array of sampler states to the geometry shader pipeline stage. |
| [ID3D11DeviceContext::GSSetShaderResources](..\d3d11\nf-d3d11-id3d11devicecontext-gssetshaderresources.md) | Bind an array of shader resources to the geometry shader stage. |
| [ID3D11DeviceContext::GSSetShader](..\d3d11\nf-d3d11-id3d11devicecontext-gssetshader.md) | Set a geometry shader to the device. |
| [ID3D11DeviceContext::GenerateMips](..\d3d11\nf-d3d11-id3d11devicecontext-generatemips.md) | Generates mipmaps for the given shader resource. |
| [ID3D11DeviceContext::GetContextFlags](..\d3d11\nf-d3d11-id3d11devicecontext-getcontextflags.md) | Gets the initialization flags associated with the current deferred context. |
| [ID3D11DeviceContext::GetData](..\d3d11\nf-d3d11-id3d11devicecontext-getdata.md) | Get data from the graphics processing unit (GPU) asynchronously. |
| [ID3D11DeviceContext::GetPredication](..\d3d11\nf-d3d11-id3d11devicecontext-getpredication.md) | Get the rendering predicate state. |
| [ID3D11DeviceContext::GetResourceMinLOD](..\d3d11\nf-d3d11-id3d11devicecontext-getresourceminlod.md) | Gets the minimum level-of-detail (LOD). |
| [ID3D11DeviceContext::GetType](..\d3d11\nf-d3d11-id3d11devicecontext-gettype.md) | Gets the type of device context. |
| [ID3D11DeviceContext::HSGetConstantBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-hsgetconstantbuffers.md) | Get the constant buffers used by the hull-shader stage. |
| [ID3D11DeviceContext::HSGetSamplers](..\d3d11\nf-d3d11-id3d11devicecontext-hsgetsamplers.md) | Get an array of sampler state interfaces from the hull-shader stage. |
| [ID3D11DeviceContext::HSGetShaderResources](..\d3d11\nf-d3d11-id3d11devicecontext-hsgetshaderresources.md) | Get the hull-shader resources. |
| [ID3D11DeviceContext::HSGetShader](..\d3d11\nf-d3d11-id3d11devicecontext-hsgetshader.md) | Get the hull shader currently set on the device. |
| [ID3D11DeviceContext::HSSetConstantBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-hssetconstantbuffers.md) | Set the constant buffers used by the hull-shader stage. |
| [ID3D11DeviceContext::HSSetSamplers](..\d3d11\nf-d3d11-id3d11devicecontext-hssetsamplers.md) | Set an array of sampler states to the hull-shader stage. |
| [ID3D11DeviceContext::HSSetShaderResources](..\d3d11\nf-d3d11-id3d11devicecontext-hssetshaderresources.md) | Bind an array of shader resources to the hull-shader stage. |
| [ID3D11DeviceContext::HSSetShader](..\d3d11\nf-d3d11-id3d11devicecontext-hssetshader.md) | Set a hull shader to the device. |
| [ID3D11DeviceContext::IAGetIndexBuffer](..\d3d11\nf-d3d11-id3d11devicecontext-iagetindexbuffer.md) | Get a pointer to the index buffer that is bound to the input-assembler stage. |
| [ID3D11DeviceContext::IAGetInputLayout](..\d3d11\nf-d3d11-id3d11devicecontext-iagetinputlayout.md) | Get a pointer to the input-layout object that is bound to the input-assembler stage. |
| [ID3D11DeviceContext::IAGetPrimitiveTopology](..\d3d11\nf-d3d11-id3d11devicecontext-iagetprimitivetopology.md) | Get information about the primitive type, and data order that describes input data for the input assembler stage. |
| [ID3D11DeviceContext::IAGetVertexBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-iagetvertexbuffers.md) | Get the vertex buffers bound to the input-assembler stage. |
| [ID3D11DeviceContext::IASetIndexBuffer](..\d3d11\nf-d3d11-id3d11devicecontext-iasetindexbuffer.md) | Bind an index buffer to the input-assembler stage. |
| [ID3D11DeviceContext::IASetInputLayout](..\d3d11\nf-d3d11-id3d11devicecontext-iasetinputlayout.md) | Bind an input-layout object to the input-assembler stage. |
| [ID3D11DeviceContext::IASetPrimitiveTopology](..\d3d11\nf-d3d11-id3d11devicecontext-iasetprimitivetopology.md) | Bind information about the primitive type, and data order that describes input data for the input assembler stage. |
| [ID3D11DeviceContext::IASetVertexBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-iasetvertexbuffers.md) | Bind an array of vertex buffers to the input-assembler stage. |
| [ID3D11DeviceContext::Map](..\d3d11\nf-d3d11-id3d11devicecontext-map.md) | Gets a pointer to the data contained in a subresource, and denies the GPU access to that subresource. |
| [ID3D11DeviceContext::OMGetBlendState](..\d3d11\nf-d3d11-id3d11devicecontext-omgetblendstate.md) | Get the blend state of the output-merger stage. |
| [ID3D11DeviceContext::OMGetDepthStencilState](..\d3d11\nf-d3d11-id3d11devicecontext-omgetdepthstencilstate.md) | Gets the depth-stencil state of the output-merger stage. |
| [ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews](..\d3d11\nf-d3d11-id3d11devicecontext-omgetrendertargetsandunorderedaccessviews.md) | Get pointers to the resources bound to the output-merger stage. |
| [ID3D11DeviceContext::OMGetRenderTargets](..\d3d11\nf-d3d11-id3d11devicecontext-omgetrendertargets.md) | Get pointers to the resources bound to the output-merger stage. |
| [ID3D11DeviceContext::OMSetBlendState](..\d3d11\nf-d3d11-id3d11devicecontext-omsetblendstate.md) | Set the blend state of the output-merger stage. |
| [ID3D11DeviceContext::OMSetDepthStencilState](..\d3d11\nf-d3d11-id3d11devicecontext-omsetdepthstencilstate.md) | Sets the depth-stencil state of the output-merger stage. |
| [ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews](..\d3d11\nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews.md) | Binds resources to the output-merger stage. |
| [ID3D11DeviceContext::OMSetRenderTargets](..\d3d11\nf-d3d11-id3d11devicecontext-omsetrendertargets.md) | Bind one or more render targets atomically and the depth-stencil buffer to the output-merger stage. |
| [ID3D11DeviceContext::PSGetConstantBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-psgetconstantbuffers.md) | Get the constant buffers used by the pixel shader pipeline stage. |
| [ID3D11DeviceContext::PSGetSamplers](..\d3d11\nf-d3d11-id3d11devicecontext-psgetsamplers.md) | Get an array of sampler states from the pixel shader pipeline stage. |
| [ID3D11DeviceContext::PSGetShaderResources](..\d3d11\nf-d3d11-id3d11devicecontext-psgetshaderresources.md) | Get the pixel shader resources. |
| [ID3D11DeviceContext::PSGetShader](..\d3d11\nf-d3d11-id3d11devicecontext-psgetshader.md) | Get the pixel shader currently set on the device. |
| [ID3D11DeviceContext::PSSetConstantBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-pssetconstantbuffers.md) | Sets the constant buffers used by the pixel shader pipeline stage. |
| [ID3D11DeviceContext::PSSetSamplers](..\d3d11\nf-d3d11-id3d11devicecontext-pssetsamplers.md) | Set an array of sampler states to the pixel shader pipeline stage. |
| [ID3D11DeviceContext::PSSetShaderResources](..\d3d11\nf-d3d11-id3d11devicecontext-pssetshaderresources.md) | Bind an array of shader resources to the pixel shader stage. |
| [ID3D11DeviceContext::PSSetShader](..\d3d11\nf-d3d11-id3d11devicecontext-pssetshader.md) | Sets a pixel shader to the device. |
| [ID3D11DeviceContext::RSGetScissorRects](..\d3d11\nf-d3d11-id3d11devicecontext-rsgetscissorrects.md) | Get the array of scissor rectangles bound to the rasterizer stage. |
| [ID3D11DeviceContext::RSGetState](..\d3d11\nf-d3d11-id3d11devicecontext-rsgetstate.md) | Get the rasterizer state from the rasterizer stage of the pipeline. |
| [ID3D11DeviceContext::RSGetViewports](..\d3d11\nf-d3d11-id3d11devicecontext-rsgetviewports.md) | Gets the array of viewports bound to the rasterizer stage. |
| [ID3D11DeviceContext::RSSetScissorRects](..\d3d11\nf-d3d11-id3d11devicecontext-rssetscissorrects.md) | Bind an array of scissor rectangles to the rasterizer stage. |
| [ID3D11DeviceContext::RSSetState](..\d3d11\nf-d3d11-id3d11devicecontext-rssetstate.md) | Set the rasterizer state for the rasterizer stage of the pipeline. |
| [ID3D11DeviceContext::RSSetViewports](..\d3d11\nf-d3d11-id3d11devicecontext-rssetviewports.md) | Bind an array of viewports to the rasterizer stage of the pipeline. |
| [ID3D11DeviceContext::ResolveSubresource](..\d3d11\nf-d3d11-id3d11devicecontext-resolvesubresource.md) | Copy a multisampled resource into a non-multisampled resource. |
| [ID3D11DeviceContext::SOGetTargets](..\d3d11\nf-d3d11-id3d11devicecontext-sogettargets.md) | Get the target output buffers for the stream-output stage of the pipeline. |
| [ID3D11DeviceContext::SOSetTargets](..\d3d11\nf-d3d11-id3d11devicecontext-sosettargets.md) | Set the target output buffers for the stream-output stage of the pipeline. |
| [ID3D11DeviceContext::SetPredication](..\d3d11\nf-d3d11-id3d11devicecontext-setpredication.md) | Set a rendering predicate. |
| [ID3D11DeviceContext::SetResourceMinLOD](..\d3d11\nf-d3d11-id3d11devicecontext-setresourceminlod.md) | Sets the minimum level-of-detail (LOD) for a resource. |
| [ID3D11DeviceContext::Unmap](..\d3d11\nf-d3d11-id3d11devicecontext-unmap.md) | Invalidate the pointer to a resource and reenable the GPU's access to that resource. |
| [ID3D11DeviceContext::UpdateSubresource](..\d3d11\nf-d3d11-id3d11devicecontext-updatesubresource.md) | The CPU copies data from memory to a subresource created in non-mappable memory. |
| [ID3D11DeviceContext::VSGetConstantBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-vsgetconstantbuffers.md) | Get the constant buffers used by the vertex shader pipeline stage. |
| [ID3D11DeviceContext::VSGetSamplers](..\d3d11\nf-d3d11-id3d11devicecontext-vsgetsamplers.md) | Get an array of sampler states from the vertex shader pipeline stage. |
| [ID3D11DeviceContext::VSGetShaderResources](..\d3d11\nf-d3d11-id3d11devicecontext-vsgetshaderresources.md) | Get the vertex shader resources. |
| [ID3D11DeviceContext::VSGetShader](..\d3d11\nf-d3d11-id3d11devicecontext-vsgetshader.md) | Get the vertex shader currently set on the device. |
| [ID3D11DeviceContext::VSSetConstantBuffers](..\d3d11\nf-d3d11-id3d11devicecontext-vssetconstantbuffers.md) | Sets the constant buffers used by the vertex shader pipeline stage. |
| [ID3D11DeviceContext::VSSetSamplers](..\d3d11\nf-d3d11-id3d11devicecontext-vssetsamplers.md) | Set an array of sampler states to the vertex shader pipeline stage. |
| [ID3D11DeviceContext::VSSetShaderResources](..\d3d11\nf-d3d11-id3d11devicecontext-vssetshaderresources.md) | Bind an array of shader resources to the vertex-shader stage. |
| [ID3D11DeviceContext::VSSetShader](..\d3d11\nf-d3d11-id3d11devicecontext-vssetshader.md) | Set a vertex shader to the device. |
| [ID3D11Fence::CreateSharedHandle](..\d3d11_3\nf-d3d11_3-id3d11fence-createsharedhandle.md) | Creates a shared handle to a fence object. |
| [ID3D11Fence::GetCompletedValue](..\d3d11_3\nf-d3d11_3-id3d11fence-getcompletedvalue.md) | Gets the current value of the fence. |
| [ID3D11Fence::SetEventOnCompletion](..\d3d11_3\nf-d3d11_3-id3d11fence-seteventoncompletion.md) | Specifies an event that should be fired when the fence reaches a certain value. |
| [ID3D11FunctionLinkingGraph::CallFunction](..\d3d11shader\nf-d3d11shader-id3d11functionlinkinggraph-callfunction.md) | Creates a call-function linking node to use in the function-linking-graph. |
| [ID3D11FunctionLinkingGraph::CreateModuleInstance](..\d3d11shader\nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance.md) | Initializes a shader module from the function-linking-graph object. |
| [ID3D11FunctionLinkingGraph::GenerateHlsl](..\d3d11shader\nf-d3d11shader-id3d11functionlinkinggraph-generatehlsl.md) | Generates Microsoft High Level Shader Language (HLSL) shader code that represents the function-linking-graph. |
| [ID3D11FunctionLinkingGraph::GetLastError](..\d3d11shader\nf-d3d11shader-id3d11functionlinkinggraph-getlasterror.md) | Gets the error from the last function call of the function-linking-graph. |
| [ID3D11FunctionLinkingGraph::PassValueWithSwizzle](..\d3d11shader\nf-d3d11shader-id3d11functionlinkinggraph-passvaluewithswizzle.md) | Passes a value with swizzle from a source linking node to a destination linking node. |
| [ID3D11FunctionLinkingGraph::PassValue](..\d3d11shader\nf-d3d11shader-id3d11functionlinkinggraph-passvalue.md) | Passes a value from a source linking node to a destination linking node. |
| [ID3D11FunctionLinkingGraph::SetInputSignature](..\d3d11shader\nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature.md) | Sets the input signature of the function-linking-graph. |
| [ID3D11FunctionLinkingGraph::SetOutputSignature](..\d3d11shader\nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature.md) | Sets the output signature of the function-linking-graph. |
| [ID3D11FunctionParameterReflection::GetDesc](..\d3d11shader\nf-d3d11shader-id3d11functionparameterreflection-getdesc.md) | Fills the parameter descriptor structure for the function's parameter. |
| [ID3D11FunctionReflection::GetConstantBufferByIndex](..\d3d11shader\nf-d3d11shader-id3d11functionreflection-getconstantbufferbyindex.md) | Gets a constant buffer by index for a function. |
| [ID3D11FunctionReflection::GetConstantBufferByName](..\d3d11shader\nf-d3d11shader-id3d11functionreflection-getconstantbufferbyname.md) | Gets a constant buffer by name for a function. |
| [ID3D11FunctionReflection::GetDesc](..\d3d11shader\nf-d3d11shader-id3d11functionreflection-getdesc.md) | Fills the function descriptor structure for the function. |
| [ID3D11FunctionReflection::GetFunctionParameter](..\d3d11shader\nf-d3d11shader-id3d11functionreflection-getfunctionparameter.md) | Gets the function parameter reflector. |
| [ID3D11FunctionReflection::GetResourceBindingDescByName](..\d3d11shader\nf-d3d11shader-id3d11functionreflection-getresourcebindingdescbyname.md) | Gets a description of how a resource is bound to a function. |
| [ID3D11FunctionReflection::GetResourceBindingDesc](..\d3d11shader\nf-d3d11shader-id3d11functionreflection-getresourcebindingdesc.md) | Gets a description of how a resource is bound to a function. |
| [ID3D11FunctionReflection::GetVariableByName](..\d3d11shader\nf-d3d11shader-id3d11functionreflection-getvariablebyname.md) | Gets a variable by name. |
| [ID3D11InfoQueue::AddApplicationMessage](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-addapplicationmessage.md) | Add a user-defined message to the message queue and send that message to debug output. |
| [ID3D11InfoQueue::AddMessage](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-addmessage.md) | Add a debug message to the message queue and send that message to debug output. |
| [ID3D11InfoQueue::AddRetrievalFilterEntries](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-addretrievalfilterentries.md) | Add storage filters to the top of the retrieval-filter stack. |
| [ID3D11InfoQueue::AddStorageFilterEntries](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-addstoragefilterentries.md) | Add storage filters to the top of the storage-filter stack. |
| [ID3D11InfoQueue::ClearRetrievalFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-clearretrievalfilter.md) | Remove a retrieval filter from the top of the retrieval-filter stack. |
| [ID3D11InfoQueue::ClearStorageFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-clearstoragefilter.md) | Remove a storage filter from the top of the storage-filter stack. |
| [ID3D11InfoQueue::ClearStoredMessages](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-clearstoredmessages.md) | Clear all messages from the message queue. |
| [ID3D11InfoQueue::GetBreakOnCategory](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getbreakoncategory.md) | Get a message category to break on when a message with that category passes through the storage filter. |
| [ID3D11InfoQueue::GetBreakOnID](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getbreakonid.md) | Get a message identifier to break on when a message with that identifier passes through the storage filter. |
| [ID3D11InfoQueue::GetBreakOnSeverity](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getbreakonseverity.md) | Get a message severity level to break on when a message with that severity level passes through the storage filter. |
| [ID3D11InfoQueue::GetMessageCountLimit](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getmessagecountlimit.md) | Get the maximum number of messages that can be added to the message queue. |
| [ID3D11InfoQueue::GetMessage](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getmessage.md) | Get a message from the message queue. |
| [ID3D11InfoQueue::GetMuteDebugOutput](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getmutedebugoutput.md) | Get a boolean that turns the debug output on or off. |
| [ID3D11InfoQueue::GetNumMessagesAllowedByStorageFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getnummessagesallowedbystoragefilter.md) | Get the number of messages that were allowed to pass through a storage filter. |
| [ID3D11InfoQueue::GetNumMessagesDeniedByStorageFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getnummessagesdeniedbystoragefilter.md) | Get the number of messages that were denied passage through a storage filter. |
| [ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getnummessagesdiscardedbymessagecountlimit.md) | Get the number of messages that were discarded due to the message count limit. |
| [ID3D11InfoQueue::GetNumStoredMessagesAllowedByRetrievalFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getnumstoredmessagesallowedbyretrievalfilter.md) | Get the number of messages that are able to pass through a retrieval filter. |
| [ID3D11InfoQueue::GetNumStoredMessages](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getnumstoredmessages.md) | Get the number of messages currently stored in the message queue. |
| [ID3D11InfoQueue::GetRetrievalFilterStackSize](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getretrievalfilterstacksize.md) | Get the size of the retrieval-filter stack in bytes. |
| [ID3D11InfoQueue::GetRetrievalFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getretrievalfilter.md) | Get the retrieval filter at the top of the retrieval-filter stack. |
| [ID3D11InfoQueue::GetStorageFilterStackSize](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getstoragefilterstacksize.md) | Get the size of the storage-filter stack in bytes. |
| [ID3D11InfoQueue::GetStorageFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-getstoragefilter.md) | Get the storage filter at the top of the storage-filter stack. |
| [ID3D11InfoQueue::PopRetrievalFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-popretrievalfilter.md) | Pop a retrieval filter from the top of the retrieval-filter stack. |
| [ID3D11InfoQueue::PopStorageFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-popstoragefilter.md) | Pop a storage filter from the top of the storage-filter stack. |
| [ID3D11InfoQueue::PushCopyOfRetrievalFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-pushcopyofretrievalfilter.md) | Push a copy of retrieval filter currently on the top of the retrieval-filter stack onto the retrieval-filter stack. |
| [ID3D11InfoQueue::PushCopyOfStorageFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-pushcopyofstoragefilter.md) | Push a copy of storage filter currently on the top of the storage-filter stack onto the storage-filter stack. |
| [ID3D11InfoQueue::PushEmptyRetrievalFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-pushemptyretrievalfilter.md) | Push an empty retrieval filter onto the retrieval-filter stack. |
| [ID3D11InfoQueue::PushEmptyStorageFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-pushemptystoragefilter.md) | Push an empty storage filter onto the storage-filter stack. |
| [ID3D11InfoQueue::PushRetrievalFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-pushretrievalfilter.md) | Push a retrieval filter onto the retrieval-filter stack. |
| [ID3D11InfoQueue::PushStorageFilter](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-pushstoragefilter.md) | Push a storage filter onto the storage-filter stack. |
| [ID3D11InfoQueue::SetBreakOnCategory](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-setbreakoncategory.md) | Set a message category to break on when a message with that category passes through the storage filter. |
| [ID3D11InfoQueue::SetBreakOnID](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-setbreakonid.md) | Set a message identifier to break on when a message with that identifier passes through the storage filter. |
| [ID3D11InfoQueue::SetBreakOnSeverity](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-setbreakonseverity.md) | Set a message severity level to break on when a message with that severity level passes through the storage filter. |
| [ID3D11InfoQueue::SetMessageCountLimit](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-setmessagecountlimit.md) | Set the maximum number of messages that can be added to the message queue. |
| [ID3D11InfoQueue::SetMuteDebugOutput](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11infoqueue-setmutedebugoutput.md) | Set a boolean that turns the debug output on or off. |
| [ID3D11LibraryReflection::GetDesc](..\d3d11shader\nf-d3d11shader-id3d11libraryreflection-getdesc.md) | Fills the library descriptor structure for the library reflection. |
| [ID3D11LibraryReflection::GetFunctionByIndex](..\d3d11shader\nf-d3d11shader-id3d11libraryreflection-getfunctionbyindex.md) | Gets the function reflector. |
| [ID3D11Linker::AddClipPlaneFromCBuffer](..\d3d11shader\nf-d3d11shader-id3d11linker-addclipplanefromcbuffer.md) | Adds a clip plane with the plane coefficients taken from a cbuffer entry for 10Level9 shaders. |
| [ID3D11Linker::Link](..\d3d11shader\nf-d3d11shader-id3d11linker-link.md) | Links the shader and produces a shader blob that the Direct3D runtime can use. |
| [ID3D11Linker::UseLibrary](..\d3d11shader\nf-d3d11shader-id3d11linker-uselibrary.md) | Adds an instance of a library module to be used for linking. |
| [ID3D11Module::CreateInstance](..\d3d11shader\nf-d3d11shader-id3d11module-createinstance.md) | Initializes an instance of a shader module that is used for resource rebinding. |
| [ID3D11ModuleInstance::BindConstantBufferByName](..\d3d11shader\nf-d3d11shader-id3d11moduleinstance-bindconstantbufferbyname.md) | Rebinds a constant buffer by name to a destination slot. |
| [ID3D11ModuleInstance::BindConstantBuffer](..\d3d11shader\nf-d3d11shader-id3d11moduleinstance-bindconstantbuffer.md) | Rebinds a constant buffer from a source slot to a destination slot. |
| [ID3D11ModuleInstance::BindResourceAsUnorderedAccessViewByName](..\d3d11shader\nf-d3d11shader-id3d11moduleinstance-bindresourceasunorderedaccessviewbyname.md) | Rebinds a resource by name as an unordered access view (UAV) to destination slots. |
| [ID3D11ModuleInstance::BindResourceAsUnorderedAccessView](..\d3d11shader\nf-d3d11shader-id3d11moduleinstance-bindresourceasunorderedaccessview.md) | Rebinds a resource as an unordered access view (UAV) from source slot to destination slot. |
| [ID3D11ModuleInstance::BindResourceByName](..\d3d11shader\nf-d3d11shader-id3d11moduleinstance-bindresourcebyname.md) | Rebinds a texture or buffer by name to destination slots. |
| [ID3D11ModuleInstance::BindResource](..\d3d11shader\nf-d3d11shader-id3d11moduleinstance-bindresource.md) | Rebinds a texture or buffer from source slot to destination slot. |
| [ID3D11ModuleInstance::BindSamplerByName](..\d3d11shader\nf-d3d11shader-id3d11moduleinstance-bindsamplerbyname.md) | Rebinds a sampler by name to destination slots. |
| [ID3D11ModuleInstance::BindSampler](..\d3d11shader\nf-d3d11shader-id3d11moduleinstance-bindsampler.md) | Rebinds a sampler from source slot to destination slot. |
| [ID3D11ModuleInstance::BindUnorderedAccessViewByName](..\d3d11shader\nf-d3d11shader-id3d11moduleinstance-bindunorderedaccessviewbyname.md) | Rebinds an unordered access view (UAV) by name to destination slots. |
| [ID3D11ModuleInstance::BindUnorderedAccessView](..\d3d11shader\nf-d3d11shader-id3d11moduleinstance-bindunorderedaccessview.md) | Rebinds an unordered access view (UAV) from source slot to destination slot. |
| [ID3D11Multithread::Enter](..\d3d11_4\nf-d3d11_4-id3d11multithread-enter.md) | Enter a device's critical section. |
| [ID3D11Multithread::GetMultithreadProtected](..\d3d11_4\nf-d3d11_4-id3d11multithread-getmultithreadprotected.md) | Find out if multithread protection is turned on or not. |
| [ID3D11Multithread::Leave](..\d3d11_4\nf-d3d11_4-id3d11multithread-leave.md) | Leave a device's critical section. |
| [ID3D11Multithread::SetMultithreadProtected](..\d3d11_4\nf-d3d11_4-id3d11multithread-setmultithreadprotected.md) | Turns multithread protection on or off. |
| [ID3D11Query1::GetDesc1](..\d3d11_3\nf-d3d11_3-id3d11query1-getdesc1.md) | Gets a query description. |
| [ID3D11Query::GetDesc](..\d3d11\nf-d3d11-id3d11query-getdesc.md) | Get a query description. |
| [ID3D11RasterizerState1::GetDesc1](..\d3d11_1\nf-d3d11_1-id3d11rasterizerstate1-getdesc1.md) | Gets the description for rasterizer state that you used to create the rasterizer-state object. |
| [ID3D11RasterizerState2::GetDesc2](..\d3d11_3\nf-d3d11_3-id3d11rasterizerstate2-getdesc2.md) | Gets the description for rasterizer state that you used to create the rasterizer-state object. |
| [ID3D11RasterizerState::GetDesc](..\d3d11\nf-d3d11-id3d11rasterizerstate-getdesc.md) | Gets the description for rasterizer state that you used to create the rasterizer-state object. |
| [ID3D11RefDefaultTrackingOptions::SetTrackingOptions](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions.md) | Sets graphics processing unit (GPU) debug reference default tracking options for specific resource types. |
| [ID3D11RefTrackingOptions::SetTrackingOptions](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11reftrackingoptions-settrackingoptions.md) | Sets graphics processing unit (GPU) debug reference tracking options. |
| [ID3D11RenderTargetView1::GetDesc1](..\d3d11_3\nf-d3d11_3-id3d11rendertargetview1-getdesc1.md) | Gets the properties of a render-target view. |
| [ID3D11RenderTargetView::GetDesc](..\d3d11\nf-d3d11-id3d11rendertargetview-getdesc.md) | Get the properties of a render target view. |
| [ID3D11Resource::GetEvictionPriority](..\d3d11\nf-d3d11-id3d11resource-getevictionpriority.md) | Get the eviction priority of a resource. |
| [ID3D11Resource::GetType](..\d3d11\nf-d3d11-id3d11resource-gettype.md) | Get the type of the resource. |
| [ID3D11Resource::SetEvictionPriority](..\d3d11\nf-d3d11-id3d11resource-setevictionpriority.md) | Set the eviction priority of a resource. |
| [ID3D11SamplerState::GetDesc](..\d3d11\nf-d3d11-id3d11samplerstate-getdesc.md) | Gets the description for sampler state that you used to create the sampler-state object. |
| [ID3D11ShaderReflection::GetBitwiseInstructionCount](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getbitwiseinstructioncount.md) | Gets the number of bitwise instructions. |
| [ID3D11ShaderReflection::GetConstantBufferByIndex](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getconstantbufferbyindex.md) | Get a constant buffer by index. |
| [ID3D11ShaderReflection::GetConstantBufferByName](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getconstantbufferbyname.md) | Get a constant buffer by name. |
| [ID3D11ShaderReflection::GetConversionInstructionCount](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getconversioninstructioncount.md) | Gets the number of conversion instructions. |
| [ID3D11ShaderReflection::GetDesc](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getdesc.md) | Get a shader description. |
| [ID3D11ShaderReflection::GetGSInputPrimitive](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getgsinputprimitive.md) | Gets the geometry-shader input-primitive description. |
| [ID3D11ShaderReflection::GetInputParameterDesc](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getinputparameterdesc.md) | Get an input-parameter description for a shader. |
| [ID3D11ShaderReflection::GetMinFeatureLevel](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getminfeaturelevel.md) | Gets the minimum feature level. |
| [ID3D11ShaderReflection::GetMovInstructionCount](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getmovinstructioncount.md) | Gets the number of Mov instructions. |
| [ID3D11ShaderReflection::GetMovcInstructionCount](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getmovcinstructioncount.md) | Gets the number of Movc instructions. |
| [ID3D11ShaderReflection::GetNumInterfaceSlots](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots.md) | Gets the number of interface slots in a shader. |
| [ID3D11ShaderReflection::GetOutputParameterDesc](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getoutputparameterdesc.md) | Get an output-parameter description for a shader. |
| [ID3D11ShaderReflection::GetPatchConstantParameterDesc](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getpatchconstantparameterdesc.md) | Get a patch-constant parameter description for a shader. |
| [ID3D11ShaderReflection::GetRequiresFlags](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getrequiresflags.md) | Gets a group of flags that indicates the requirements of a shader. |
| [ID3D11ShaderReflection::GetResourceBindingDescByName](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getresourcebindingdescbyname.md) | Get a description of how a resource is bound to a shader. |
| [ID3D11ShaderReflection::GetResourceBindingDesc](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getresourcebindingdesc.md) | Get a description of how a resource is bound to a shader. |
| [ID3D11ShaderReflection::GetThreadGroupSize](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getthreadgroupsize.md) | Retrieves the sizes, in units of threads, of the X, Y, and Z dimensions of the shader's thread-group grid. |
| [ID3D11ShaderReflection::GetVariableByName](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-getvariablebyname.md) | Gets a variable by name. |
| [ID3D11ShaderReflection::IsSampleFrequencyShader](..\d3d11shader\nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader.md) | Indicates whether a shader is a sample frequency shader. |
| [ID3D11ShaderReflectionConstantBuffer::GetDesc](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectionconstantbuffer-getdesc.md) | Get a constant-buffer description. |
| [ID3D11ShaderReflectionConstantBuffer::GetVariableByIndex](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectionconstantbuffer-getvariablebyindex.md) | Get a shader-reflection variable by index. |
| [ID3D11ShaderReflectionConstantBuffer::GetVariableByName](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectionconstantbuffer-getvariablebyname.md) | Get a shader-reflection variable by name. |
| [ID3D11ShaderReflectionType::GetBaseClass](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectiontype-getbaseclass.md) | Gets an ID3D11ShaderReflectionType Interface interface containing the variable base class type. |
| [ID3D11ShaderReflectionType::GetDesc](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectiontype-getdesc.md) | Get the description of a shader-reflection-variable type. |
| [ID3D11ShaderReflectionType::GetInterfaceByIndex](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectiontype-getinterfacebyindex.md) | Get an interface by index. |
| [ID3D11ShaderReflectionType::GetMemberTypeByIndex](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectiontype-getmembertypebyindex.md) | Get a shader-reflection-variable type by index. |
| [ID3D11ShaderReflectionType::GetMemberTypeByName](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectiontype-getmembertypebyname.md) | Get a shader-reflection-variable type by name. |
| [ID3D11ShaderReflectionType::GetMemberTypeName](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectiontype-getmembertypename.md) | Get a shader-reflection-variable type. |
| [ID3D11ShaderReflectionType::GetNumInterfaces](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectiontype-getnuminterfaces.md) | Gets the number of interfaces. |
| [ID3D11ShaderReflectionType::GetSubType](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectiontype-getsubtype.md) | Gets the base class of a class. |
| [ID3D11ShaderReflectionType::ImplementsInterface](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectiontype-implementsinterface.md) | Indicates whether a class type implements an interface. |
| [ID3D11ShaderReflectionType::IsEqual](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectiontype-isequal.md) | Indicates whether two ID3D11ShaderReflectionType Interface pointers have the same underlying type. |
| [ID3D11ShaderReflectionType::IsOfType](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectiontype-isoftype.md) | Indicates whether a variable is of the specified type. |
| [ID3D11ShaderReflectionVariable::GetBuffer](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectionvariable-getbuffer.md) | This method returns the buffer of the current ID3D11ShaderReflectionVariable. |
| [ID3D11ShaderReflectionVariable::GetDesc](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectionvariable-getdesc.md) | Get a shader-variable description. |
| [ID3D11ShaderReflectionVariable::GetInterfaceSlot](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot.md) | Gets the corresponding interface slot for a variable that represents an interface pointer. |
| [ID3D11ShaderReflectionVariable::GetType](..\d3d11shader\nf-d3d11shader-id3d11shaderreflectionvariable-gettype.md) | Get a shader-variable type. |
| [ID3D11ShaderResourceView1::GetDesc1](..\d3d11_3\nf-d3d11_3-id3d11shaderresourceview1-getdesc1.md) | Gets the shader-resource view's description. |
| [ID3D11ShaderResourceView::GetDesc](..\d3d11\nf-d3d11-id3d11shaderresourceview-getdesc.md) | Get the shader resource view's description. |
| [ID3D11ShaderTrace::GetInitialRegisterContents](..\d3d11shadertracing\nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents.md) | Retrieves the initial contents of the specified input register. |
| [ID3D11ShaderTrace::GetReadRegister](..\d3d11shadertracing\nf-d3d11shadertracing-id3d11shadertrace-getreadregister.md) | Retrieves information about a register that was read by a step in the trace. |
| [ID3D11ShaderTrace::GetStep](..\d3d11shadertracing\nf-d3d11shadertracing-id3d11shadertrace-getstep.md) | Retrieves information about the specified step in the trace. |
| [ID3D11ShaderTrace::GetTraceStats](..\d3d11shadertracing\nf-d3d11shadertracing-id3d11shadertrace-gettracestats.md) | Returns statistics about the trace. |
| [ID3D11ShaderTrace::GetWrittenRegister](..\d3d11shadertracing\nf-d3d11shadertracing-id3d11shadertrace-getwrittenregister.md) | Retrieves information about a register that was written by a step in the trace. |
| [ID3D11ShaderTrace::PSSelectStamp](..\d3d11shadertracing\nf-d3d11shadertracing-id3d11shadertrace-psselectstamp.md) | Sets the specified pixel-shader stamp. |
| [ID3D11ShaderTrace::ResetTrace](..\d3d11shadertracing\nf-d3d11shadertracing-id3d11shadertrace-resettrace.md) | Resets the shader-trace object. |
| [ID3D11ShaderTrace::TraceReady](..\d3d11shadertracing\nf-d3d11shadertracing-id3d11shadertrace-traceready.md) | Specifies that the shader trace recorded and is ready to use. |
| [ID3D11ShaderTraceFactory::CreateShaderTrace](..\d3d11shadertracing\nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace.md) | Creates a shader-trace interface for a shader-trace information object. |
| [ID3D11SwitchToRef::GetUseRef](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11switchtoref-getuseref.md) | ID3D11SwitchToRef |
| [ID3D11SwitchToRef::SetUseRef](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11switchtoref-setuseref.md) | ID3D11SwitchToRef |
| [ID3D11Texture1D::GetDesc](..\d3d11\nf-d3d11-id3d11texture1d-getdesc.md) | Get the properties of the texture resource. |
| [ID3D11Texture2D1::GetDesc1](..\d3d11_3\nf-d3d11_3-id3d11texture2d1-getdesc1.md) | Gets the properties of the texture resource. |
| [ID3D11Texture2D::GetDesc](..\d3d11\nf-d3d11-id3d11texture2d-getdesc.md) | Get the properties of the texture resource. |
| [ID3D11Texture3D1::GetDesc1](..\d3d11_3\nf-d3d11_3-id3d11texture3d1-getdesc1.md) | Gets the properties of the texture resource. |
| [ID3D11Texture3D::GetDesc](..\d3d11\nf-d3d11-id3d11texture3d-getdesc.md) | Get the properties of the texture resource. |
| [ID3D11TracingDevice::SetShaderTrackingOptionsByType](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype.md) | Sets the reference rasterizer's default race-condition tracking options for the specified resource types. |
| [ID3D11TracingDevice::SetShaderTrackingOptions](..\d3d11sdklayers\nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptions.md) | Sets the reference rasterizer's race-condition tracking options for a specific shader. |
| [ID3D11UnorderedAccessView1::GetDesc1](..\d3d11_3\nf-d3d11_3-id3d11unorderedaccessview1-getdesc1.md) | Gets a description of the resource. |
| [ID3D11UnorderedAccessView::GetDesc](..\d3d11\nf-d3d11-id3d11unorderedaccessview-getdesc.md) | Get a description of the resource. |
| [ID3D11View::GetResource](..\d3d11\nf-d3d11-id3d11view-getresource.md) | Get the resource that is accessed through this view. |
| [ID3DUserDefinedAnnotation::BeginEvent](..\d3d11_1\nf-d3d11_1-id3duserdefinedannotation-beginevent.md) | Marks the beginning of a section of event code. |
| [ID3DUserDefinedAnnotation::EndEvent](..\d3d11_1\nf-d3d11_1-id3duserdefinedannotation-endevent.md) | Marks the end of a section of event code. |
| [ID3DUserDefinedAnnotation::GetStatus](..\d3d11_1\nf-d3d11_1-id3duserdefinedannotation-getstatus.md) | Determines whether the calling application is running under a Microsoft Direct3D profiling tool. |
| [ID3DUserDefinedAnnotation::SetMarker](..\d3d11_1\nf-d3d11_1-id3duserdefinedannotation-setmarker.md) | Marks a single point of execution in code. |
| [ID3DX11FFT::AttachBuffersAndPrecompute](..\d3dcsx\nf-d3dcsx-id3dx11fft-attachbuffersandprecompute.md) | Attaches buffers to an FFT context and performs any required precomputations. |
| [ID3DX11FFT::ForwardTransform](..\d3dcsx\nf-d3dcsx-id3dx11fft-forwardtransform.md) | Performs a forward FFT. |
| [ID3DX11FFT::GetForwardScale](..\d3dcsx\nf-d3dcsx-id3dx11fft-getforwardscale.md) | Gets the scale for forward transforms. |
| [ID3DX11FFT::GetInverseScale](..\d3dcsx\nf-d3dcsx-id3dx11fft-getinversescale.md) | Get the scale for inverse transforms. |
| [ID3DX11FFT::InverseTransform](..\d3dcsx\nf-d3dcsx-id3dx11fft-inversetransform.md) | Performs an inverse FFT. |
| [ID3DX11FFT::SetForwardScale](..\d3dcsx\nf-d3dcsx-id3dx11fft-setforwardscale.md) | Sets the scale used for forward transforms. |
| [ID3DX11FFT::SetInverseScale](..\d3dcsx\nf-d3dcsx-id3dx11fft-setinversescale.md) | Sets the scale used for inverse transforms. |
| [ID3DX11Scan::Multiscan](..\d3dcsx\nf-d3dcsx-id3dx11scan-multiscan.md) | Performs a multiscan of a sequence. |
| [ID3DX11Scan::Scan](..\d3dcsx\nf-d3dcsx-id3dx11scan-scan.md) | Performs an unsegmented scan of a sequence. |
| [ID3DX11Scan::SetScanDirection](..\d3dcsx\nf-d3dcsx-id3dx11scan-setscandirection.md) | Sets which direction to perform scans in. |
| [ID3DX11SegmentedScan::SegScan](..\d3dcsx\nf-d3dcsx-id3dx11segmentedscan-segscan.md) | Performs a segmented scan of a sequence. |
| [ID3DX11SegmentedScan::SetScanDirection](..\d3dcsx\nf-d3dcsx-id3dx11segmentedscan-setscandirection.md) | Sets which direction to perform scans in. |
