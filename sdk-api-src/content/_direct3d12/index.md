---
UID: TP:direct3d12
ms.assetid: 7a701202-f29f-3d16-a1f3-84c2485de6f5
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Direct3D 12 Graphics



Overview of the Direct3D 12 Graphics technology.

To develop Direct3D 12 Graphics, you need these headers:

 * [d3d11on12.h](..\d3d11on12\index.md)
 * [d3d12.h](..\d3d12\index.md)
 * [d3d12sdklayers.h](..\d3d12sdklayers\index.md)
 * [d3d12shader.h](..\d3d12shader\index.md)

For the programming guide, see [Direct3D 12 Graphics](/windows/desktop/direct3d12).

## Functions

| Title   | Description   |
| ---- |:---- |
| [D3D11On12CreateDevice function](..\d3d11on12\nf-d3d11on12-d3d11on12createdevice.md) | Creates a device that uses Direct3D 11 functionality in Direct3D 12, specifying a pre-existing D3D12 device to use for D3D11 interop. |
| [D3D12CreateDevice function](..\d3d12\nf-d3d12-d3d12createdevice.md) | Creates a device that represents the display adapter. |
| [D3D12CreateRootSignatureDeserializer function](..\d3d12\nf-d3d12-d3d12createrootsignaturedeserializer.md) | Deserializes a root signature so you can determine the layout definition (D3D12_ROOT_SIGNATURE_DESC). |
| [D3D12CreateVersionedRootSignatureDeserializer function](..\d3d12\nf-d3d12-d3d12createversionedrootsignaturedeserializer.md) | Generates an interface that can return the deserialized data structure, via GetUnconvertedRootSignatureDesc. |
| [D3D12EnableExperimentalFeatures function](..\d3d12\nf-d3d12-d3d12enableexperimentalfeatures.md) | Enables a list of experimental features. |
| [D3D12GetDebugInterface function](..\d3d12\nf-d3d12-d3d12getdebuginterface.md) | Gets a debug interface. |
| [D3D12SerializeRootSignature function](..\d3d12\nf-d3d12-d3d12serializerootsignature.md) | Serializes a root signature version 1.0 that can be passed to ID3D12Device |
| [D3D12SerializeVersionedRootSignature function](..\d3d12\nf-d3d12-d3d12serializeversionedrootsignature.md) | Serializes a root signature of any version that can be passed to ID3D12Device |

## Structures

| Title   | Description   |
| ---- |:---- |
| [D3D11_RESOURCE_FLAGS structure](..\d3d11on12\ns-d3d11on12-d3d11_resource_flags.md) | Used with ID3D11On12Device |
| [D3D12_BLEND_DESC structure](..\d3d12\ns-d3d12-d3d12_blend_desc.md) | Describes the blend state. |
| [D3D12_BOX structure](..\d3d12\ns-d3d12-d3d12_box.md) | Describes a 3D box. |
| [D3D12_BUFFER_RTV structure](..\d3d12\ns-d3d12-d3d12_buffer_rtv.md) | Describes the elements in a buffer resource to use in a render-target view. |
| [D3D12_BUFFER_SRV structure](..\d3d12\ns-d3d12-d3d12_buffer_srv.md) | Describes the elements in a buffer resource to use in a shader-resource view. |
| [D3D12_BUFFER_UAV structure](..\d3d12\ns-d3d12-d3d12_buffer_uav.md) | Describes the elements in a buffer to use in a unordered-access view. |
| [D3D12_CACHED_PIPELINE_STATE structure](..\d3d12\ns-d3d12-d3d12_cached_pipeline_state.md) | Stores a pipeline state. |
| [D3D12_CLEAR_VALUE structure](..\d3d12\ns-d3d12-d3d12_clear_value.md) | Describes a value used to optimize clear operations for a particular resource. |
| [D3D12_COMMAND_QUEUE_DESC structure](..\d3d12\ns-d3d12-d3d12_command_queue_desc.md) | Describes a command queue. |
| [D3D12_COMMAND_SIGNATURE_DESC structure](..\d3d12\ns-d3d12-d3d12_command_signature_desc.md) | Describes the arguments (parameters) of a command signature. |
| [D3D12_COMPUTE_PIPELINE_STATE_DESC structure](..\d3d12\ns-d3d12-d3d12_compute_pipeline_state_desc.md) | Describes a compute pipeline state object. |
| [D3D12_CONSTANT_BUFFER_VIEW_DESC structure](..\d3d12\ns-d3d12-d3d12_constant_buffer_view_desc.md) | Describes a constant buffer to view. |
| [D3D12_CPU_DESCRIPTOR_HANDLE structure](..\d3d12\ns-d3d12-d3d12_cpu_descriptor_handle.md) | Describes a CPU descriptor handle. |
| [D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS structure](..\d3d12sdklayers\ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings.md) | Describes per-command-list settings used by GPU-Based Validation. |
| [D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS structure](..\d3d12sdklayers\ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings.md) | Describes settings used by GPU-Based Validation. |
| [D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR structure](..\d3d12sdklayers\ns-d3d12sdklayers-d3d12_debug_device_gpu_slowdown_performance_factor.md) | Describes the amount of artificial slowdown inserted by the debug device to simulate lower-performance graphics adapters. |
| [D3D12_DEPTH_STENCILOP_DESC structure](..\d3d12\ns-d3d12-d3d12_depth_stencilop_desc.md) | Describes stencil operations that can be performed based on the results of stencil test. |
| [D3D12_DEPTH_STENCIL_DESC structure](..\d3d12\ns-d3d12-d3d12_depth_stencil_desc.md) | Describes depth-stencil state. |
| [D3D12_DEPTH_STENCIL_DESC1 structure](..\d3d12\ns-d3d12-d3d12_depth_stencil_desc1.md) | Describes depth-stencil state. |
| [D3D12_DEPTH_STENCIL_VALUE structure](..\d3d12\ns-d3d12-d3d12_depth_stencil_value.md) | Specifies a depth and stencil value. |
| [D3D12_DEPTH_STENCIL_VIEW_DESC structure](..\d3d12\ns-d3d12-d3d12_depth_stencil_view_desc.md) | Describes the subresources of a texture that are accessible from a depth-stencil view. |
| [D3D12_DESCRIPTOR_HEAP_DESC structure](..\d3d12\ns-d3d12-d3d12_descriptor_heap_desc.md) | Describes the descriptor heap. |
| [D3D12_DESCRIPTOR_RANGE structure](..\d3d12\ns-d3d12-d3d12_descriptor_range.md) | Describes a descriptor range. |
| [D3D12_DESCRIPTOR_RANGE1 structure](..\d3d12\ns-d3d12-d3d12_descriptor_range1.md) | Describes a descriptor range, with flags to determine their volatility. |
| [D3D12_DISCARD_REGION structure](..\d3d12\ns-d3d12-d3d12_discard_region.md) | Describes details for the discard-resource operation. |
| [D3D12_DISPATCH_ARGUMENTS structure](..\d3d12\ns-d3d12-d3d12_dispatch_arguments.md) | Describes dispatch parameters, for use by the compute shader. |
| [D3D12_DRAW_ARGUMENTS structure](..\d3d12\ns-d3d12-d3d12_draw_arguments.md) | Describes parameters for drawing instances. |
| [D3D12_DRAW_INDEXED_ARGUMENTS structure](..\d3d12\ns-d3d12-d3d12_draw_indexed_arguments.md) | Describes parameters for drawing indexed instances. |
| [D3D12_FEATURE_DATA_ARCHITECTURE structure](..\d3d12\ns-d3d12-d3d12_feature_data_architecture.md) | Provide detail about the adapter architecture, helping applications better optimize for certain adapter properties. |
| [D3D12_FEATURE_DATA_ARCHITECTURE1 structure](..\d3d12\ns-d3d12-d3d12_feature_data_architecture1.md) | Provide detail about the adapter architecture, helping applications better optimize for certain adapter properties. |
| [D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY structure](..\d3d12\ns-d3d12-d3d12_feature_data_command_queue_priority.md) | Details the adapter's support for prioritization of different command queue types. |
| [D3D12_FEATURE_DATA_D3D12_OPTIONS structure](..\d3d12\ns-d3d12-d3d12_feature_data_d3d12_options.md) | Describes Direct3D 12 feature options in the current graphics driver. |
| [D3D12_FEATURE_DATA_D3D12_OPTIONS1 structure](..\d3d12\ns-d3d12-d3d12_feature_data_d3d12_options1.md) | Describes the level of support for HLSL 6.0 wave operations. |
| [D3D12_FEATURE_DATA_D3D12_OPTIONS2 structure](..\d3d12\ns-d3d12-d3d12_feature_data_d3d12_options2.md) | Details the adapter's support for certain optional features of Direct3D 12. |
| [D3D12_FEATURE_DATA_D3D12_OPTIONS3 structure](..\d3d12\ns-d3d12-d3d12_feature_data_d3d12_options3.md) | Used to indicate the level of support that the adapter provides for optional features of Direct3D 12. |
| [D3D12_FEATURE_DATA_EXISTING_HEAPS structure](..\d3d12\ns-d3d12-d3d12_feature_data_existing_heaps.md) | Used to determinine whether the adapter supports creating heaps from existing system memory. |
| [D3D12_FEATURE_DATA_FEATURE_LEVELS structure](..\d3d12\ns-d3d12-d3d12_feature_data_feature_levels.md) | Describes info about the feature levels supported by the current graphics driver. |
| [D3D12_FEATURE_DATA_FORMAT_INFO structure](..\d3d12\ns-d3d12-d3d12_feature_data_format_info.md) | Describes the DXGI data format. |
| [D3D12_FEATURE_DATA_FORMAT_SUPPORT structure](..\d3d12\ns-d3d12-d3d12_feature_data_format_support.md) | Describes which resources are supported by the current graphics driver for a given format. |
| [D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT structure](..\d3d12\ns-d3d12-d3d12_feature_data_gpu_virtual_address_support.md) | Details the adapter's GPU virtual address space limitations, including maximum address bits per resource and per process. |
| [D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS structure](..\d3d12\ns-d3d12-d3d12_feature_data_multisample_quality_levels.md) | Describes the image quality levels for a given format and sample count. |
| [D3D12_FEATURE_DATA_ROOT_SIGNATURE structure](..\d3d12\ns-d3d12-d3d12_feature_data_root_signature.md) | Pass this structure to CheckFeatureSupport to check for root signature version support. |
| [D3D12_FEATURE_DATA_SHADER_CACHE structure](..\d3d12\ns-d3d12-d3d12_feature_data_shader_cache.md) | Describes the level of shader caching supported in the current graphics driver. |
| [D3D12_FEATURE_DATA_SHADER_MODEL structure](..\d3d12\ns-d3d12-d3d12_feature_data_shader_model.md) | Contains the supported shader model. |
| [D3D12_GPU_DESCRIPTOR_HANDLE structure](..\d3d12\ns-d3d12-d3d12_gpu_descriptor_handle.md) | Describes a GPU descriptor handle. |
| [D3D12_GRAPHICS_PIPELINE_STATE_DESC structure](..\d3d12\ns-d3d12-d3d12_graphics_pipeline_state_desc.md) | Describes a graphics pipeline state object. |
| [D3D12_HEAP_DESC structure](..\d3d12\ns-d3d12-d3d12_heap_desc.md) | Describes a heap. |
| [D3D12_HEAP_PROPERTIES structure](..\d3d12\ns-d3d12-d3d12_heap_properties.md) | Describes heap properties. |
| [D3D12_INDEX_BUFFER_VIEW structure](..\d3d12\ns-d3d12-d3d12_index_buffer_view.md) | Describes the index buffer to view. |
| [D3D12_INDIRECT_ARGUMENT_DESC structure](..\d3d12\ns-d3d12-d3d12_indirect_argument_desc.md) | Describes an indirect argument (an indirect parameter), for use with a command signature. |
| [D3D12_INFO_QUEUE_FILTER structure](..\d3d12sdklayers\ns-d3d12sdklayers-d3d12_info_queue_filter.md) | Debug message filter; contains a lists of message types to allow or deny. |
| [D3D12_INFO_QUEUE_FILTER_DESC structure](..\d3d12sdklayers\ns-d3d12sdklayers-d3d12_info_queue_filter_desc.md) | Allow or deny certain types of messages to pass through a filter. |
| [D3D12_INPUT_ELEMENT_DESC structure](..\d3d12\ns-d3d12-d3d12_input_element_desc.md) | Describes a single element for the input-assembler stage of the graphics pipeline. |
| [D3D12_INPUT_LAYOUT_DESC structure](..\d3d12\ns-d3d12-d3d12_input_layout_desc.md) | Describes the input-buffer data for the input-assembler stage. |
| [D3D12_MEMCPY_DEST structure](..\d3d12\ns-d3d12-d3d12_memcpy_dest.md) | Describes the destination of a memory copy operation. |
| [D3D12_MESSAGE structure](..\d3d12sdklayers\ns-d3d12sdklayers-d3d12_message.md) | A debug message in the Information Queue. |
| [D3D12_PACKED_MIP_INFO structure](..\d3d12\ns-d3d12-d3d12_packed_mip_info.md) | Describes the tile structure of a tiled resource with mipmaps. |
| [D3D12_PIPELINE_STATE_STREAM_DESC structure](..\d3d12\ns-d3d12-d3d12_pipeline_state_stream_desc.md) | Describes a pipeline state stream. |
| [D3D12_PLACED_SUBRESOURCE_FOOTPRINT structure](..\d3d12\ns-d3d12-d3d12_placed_subresource_footprint.md) | Describes the footprint of a placed subresource, including the offset and the D3D12_SUBRESOURCE_FOOTPRINT. |
| [D3D12_QUERY_DATA_PIPELINE_STATISTICS structure](..\d3d12\ns-d3d12-d3d12_query_data_pipeline_statistics.md) | Query information about graphics-pipeline activity in between calls to BeginQuery and EndQuery. |
| [D3D12_QUERY_DATA_SO_STATISTICS structure](..\d3d12\ns-d3d12-d3d12_query_data_so_statistics.md) | Describes query data for stream output. |
| [D3D12_QUERY_HEAP_DESC structure](..\d3d12\ns-d3d12-d3d12_query_heap_desc.md) | Describes the purpose of a query heap. A query heap contains an array of individual queries. |
| [D3D12_RANGE structure](..\d3d12\ns-d3d12-d3d12_range.md) | Describes a memory range. |
| [D3D12_RANGE_UINT64 structure](..\d3d12\ns-d3d12-d3d12_range_uint64.md) | Describes a memory range in a 64-bit address space. |
| [D3D12_RASTERIZER_DESC structure](..\d3d12\ns-d3d12-d3d12_rasterizer_desc.md) | Describes rasterizer state. |
| [D3D12_RENDER_TARGET_BLEND_DESC structure](..\d3d12\ns-d3d12-d3d12_render_target_blend_desc.md) | Describes the blend state for a render target. |
| [D3D12_RENDER_TARGET_VIEW_DESC structure](..\d3d12\ns-d3d12-d3d12_render_target_view_desc.md) | Describes the subresources from a resource that are accessible by using a render-target view. |
| [D3D12_RESOURCE_ALIASING_BARRIER structure](..\d3d12\ns-d3d12-d3d12_resource_aliasing_barrier.md) | Describes the transition between usages of two different resources that have mappings into the same heap. |
| [D3D12_RESOURCE_ALLOCATION_INFO structure](..\d3d12\ns-d3d12-d3d12_resource_allocation_info.md) | Describes parameters needed to allocate resources. |
| [D3D12_RESOURCE_BARRIER structure](..\d3d12\ns-d3d12-d3d12_resource_barrier.md) | Describes a resource barrier (transition in resource use). |
| [D3D12_RESOURCE_DESC structure](..\d3d12\ns-d3d12-d3d12_resource_desc.md) | Describes a resource, such as a texture. This structure is used extensively. |
| [D3D12_RESOURCE_TRANSITION_BARRIER structure](..\d3d12\ns-d3d12-d3d12_resource_transition_barrier.md) | Describes the transition of subresources between different usages. |
| [D3D12_RESOURCE_UAV_BARRIER structure](..\d3d12\ns-d3d12-d3d12_resource_uav_barrier.md) | Represents a resource in which all UAV accesses must complete before any future UAV accesses can begin. |
| [D3D12_ROOT_CONSTANTS structure](..\d3d12\ns-d3d12-d3d12_root_constants.md) | Describes constants inline in the root signature that appear in shaders as one constant buffer. |
| [D3D12_ROOT_DESCRIPTOR structure](..\d3d12\ns-d3d12-d3d12_root_descriptor.md) | Describes descriptors inline in the root signature version 1.0 that appear in shaders. |
| [D3D12_ROOT_DESCRIPTOR1 structure](..\d3d12\ns-d3d12-d3d12_root_descriptor1.md) | Describes descriptors inline in the root signature version 1.1 that appear in shaders. |
| [D3D12_ROOT_DESCRIPTOR_TABLE structure](..\d3d12\ns-d3d12-d3d12_root_descriptor_table.md) | Describes the root signature 1.0 layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap. |
| [D3D12_ROOT_DESCRIPTOR_TABLE1 structure](..\d3d12\ns-d3d12-d3d12_root_descriptor_table1.md) | Describes the root signature 1.1 layout of a descriptor table as a collection of descriptor ranges that appear one after the other in a descriptor heap. |
| [D3D12_ROOT_PARAMETER structure](..\d3d12\ns-d3d12-d3d12_root_parameter.md) | Describes the slot of a root signature version 1.0. |
| [D3D12_ROOT_PARAMETER1 structure](..\d3d12\ns-d3d12-d3d12_root_parameter1.md) | Describes the slot of a root signature version 1.1. |
| [D3D12_ROOT_SIGNATURE_DESC structure](..\d3d12\ns-d3d12-d3d12_root_signature_desc.md) | Describes the layout of a root signature version 1.0. |
| [D3D12_ROOT_SIGNATURE_DESC1 structure](..\d3d12\ns-d3d12-d3d12_root_signature_desc1.md) | Describes the layout of a root signature version 1.1. |
| [D3D12_RT_FORMAT_ARRAY structure](..\d3d12\ns-d3d12-d3d12_rt_format_array.md) | Wraps an array of render target formats. |
| [D3D12_SAMPLER_DESC structure](..\d3d12\ns-d3d12-d3d12_sampler_desc.md) | Describes a sampler state. |
| [D3D12_SAMPLE_POSITION structure](..\d3d12\ns-d3d12-d3d12_sample_position.md) | Describes a sub-pixel sample position for use with programmable sample positions. |
| [D3D12_SHADER_BYTECODE structure](..\d3d12\ns-d3d12-d3d12_shader_bytecode.md) | Describes shader data. |
| [D3D12_SHADER_RESOURCE_VIEW_DESC structure](..\d3d12\ns-d3d12-d3d12_shader_resource_view_desc.md) | Describes a shader-resource view. |
| [D3D12_SO_DECLARATION_ENTRY structure](..\d3d12\ns-d3d12-d3d12_so_declaration_entry.md) | Describes a vertex element in a vertex buffer in an output slot. |
| [D3D12_STATIC_SAMPLER_DESC structure](..\d3d12\ns-d3d12-d3d12_static_sampler_desc.md) | Describes a static sampler. |
| [D3D12_STREAM_OUTPUT_BUFFER_VIEW structure](..\d3d12\ns-d3d12-d3d12_stream_output_buffer_view.md) | Describes a stream output buffer. |
| [D3D12_STREAM_OUTPUT_DESC structure](..\d3d12\ns-d3d12-d3d12_stream_output_desc.md) | Describes a streaming output buffer. |
| [D3D12_SUBRESOURCE_DATA structure](..\d3d12\ns-d3d12-d3d12_subresource_data.md) | Describes subresource data. |
| [D3D12_SUBRESOURCE_FOOTPRINT structure](..\d3d12\ns-d3d12-d3d12_subresource_footprint.md) | Describes the format, width, height, depth, and row-pitch of the subresource into the parent resource. |
| [D3D12_SUBRESOURCE_INFO structure](..\d3d12\ns-d3d12-d3d12_subresource_info.md) | Describes subresource data. |
| [D3D12_SUBRESOURCE_RANGE_UINT64 structure](..\d3d12\ns-d3d12-d3d12_subresource_range_uint64.md) | Describes a subresource memory range. |
| [D3D12_SUBRESOURCE_TILING structure](..\d3d12\ns-d3d12-d3d12_subresource_tiling.md) | Describes a tiled subresource volume. |
| [D3D12_TEX1D_ARRAY_DSV structure](..\d3d12\ns-d3d12-d3d12_tex1d_array_dsv.md) | Describes the subresources from an array of 1D textures to use in a depth-stencil view. |
| [D3D12_TEX1D_ARRAY_RTV structure](..\d3d12\ns-d3d12-d3d12_tex1d_array_rtv.md) | Describes the subresources from an array of 1D textures to use in a render-target view. |
| [D3D12_TEX1D_ARRAY_SRV structure](..\d3d12\ns-d3d12-d3d12_tex1d_array_srv.md) | Describes the subresources from an array of 1D textures to use in a shader-resource view. |
| [D3D12_TEX1D_ARRAY_UAV structure](..\d3d12\ns-d3d12-d3d12_tex1d_array_uav.md) | Describes an array of unordered-access 1D texture resources. |
| [D3D12_TEX1D_DSV structure](..\d3d12\ns-d3d12-d3d12_tex1d_dsv.md) | Describes the subresource from a 1D texture that is accessible to a depth-stencil view. |
| [D3D12_TEX1D_RTV structure](..\d3d12\ns-d3d12-d3d12_tex1d_rtv.md) | Describes the subresource from a 1D texture to use in a render-target view. |
| [D3D12_TEX1D_SRV structure](..\d3d12\ns-d3d12-d3d12_tex1d_srv.md) | Specifies the subresource from a 1D texture to use in a shader-resource view. |
| [D3D12_TEX1D_UAV structure](..\d3d12\ns-d3d12-d3d12_tex1d_uav.md) | Describes a unordered-access 1D texture resource. |
| [D3D12_TEX2DMS_ARRAY_DSV structure](..\d3d12\ns-d3d12-d3d12_tex2dms_array_dsv.md) | Describes the subresources from an array of multi sampled 2D textures for a depth-stencil view. |
| [D3D12_TEX2DMS_ARRAY_RTV structure](..\d3d12\ns-d3d12-d3d12_tex2dms_array_rtv.md) | Describes the subresources from an array of multi sampled 2D textures to use in a render-target view. |
| [D3D12_TEX2DMS_ARRAY_SRV structure](..\d3d12\ns-d3d12-d3d12_tex2dms_array_srv.md) | Describes the subresources from an array of multi sampled 2D textures to use in a shader-resource view. |
| [D3D12_TEX2DMS_DSV structure](..\d3d12\ns-d3d12-d3d12_tex2dms_dsv.md) | Describes the subresource from a multi sampled 2D texture that is accessible to a depth-stencil view. |
| [D3D12_TEX2DMS_RTV structure](..\d3d12\ns-d3d12-d3d12_tex2dms_rtv.md) | Describes the subresource from a multi sampled 2D texture to use in a render-target view. |
| [D3D12_TEX2DMS_SRV structure](..\d3d12\ns-d3d12-d3d12_tex2dms_srv.md) | Describes the subresources from a multi sampled 2D texture to use in a shader-resource view. |
| [D3D12_TEX2D_ARRAY_DSV structure](..\d3d12\ns-d3d12-d3d12_tex2d_array_dsv.md) | Describes the subresources from an array of 2D textures that are accessible to a depth-stencil view. |
| [D3D12_TEX2D_ARRAY_RTV structure](..\d3d12\ns-d3d12-d3d12_tex2d_array_rtv.md) | Describes the subresources from an array of 2D textures to use in a render-target view. |
| [D3D12_TEX2D_ARRAY_SRV structure](..\d3d12\ns-d3d12-d3d12_tex2d_array_srv.md) | Describes the subresources from an array of 2D textures to use in a shader-resource view. |
| [D3D12_TEX2D_ARRAY_UAV structure](..\d3d12\ns-d3d12-d3d12_tex2d_array_uav.md) | Describes an array of unordered-access 2D texture resources. |
| [D3D12_TEX2D_DSV structure](..\d3d12\ns-d3d12-d3d12_tex2d_dsv.md) | Describes the subresource from a 2D texture that is accessible to a depth-stencil view. |
| [D3D12_TEX2D_RTV structure](..\d3d12\ns-d3d12-d3d12_tex2d_rtv.md) | Describes the subresource from a 2D texture to use in a render-target view. |
| [D3D12_TEX2D_SRV structure](..\d3d12\ns-d3d12-d3d12_tex2d_srv.md) | Describes the subresource from a 2D texture to use in a shader-resource view. |
| [D3D12_TEX2D_UAV structure](..\d3d12\ns-d3d12-d3d12_tex2d_uav.md) | Describes a unordered-access 2D texture resource. |
| [D3D12_TEX3D_RTV structure](..\d3d12\ns-d3d12-d3d12_tex3d_rtv.md) | Describes the subresources from a 3D texture to use in a render-target view. |
| [D3D12_TEX3D_SRV structure](..\d3d12\ns-d3d12-d3d12_tex3d_srv.md) | Describes the subresources from a 3D texture to use in a shader-resource view. |
| [D3D12_TEX3D_UAV structure](..\d3d12\ns-d3d12-d3d12_tex3d_uav.md) | Describes a unordered-access 3D texture resource. |
| [D3D12_TEXCUBE_ARRAY_SRV structure](..\d3d12\ns-d3d12-d3d12_texcube_array_srv.md) | Describes the subresources from an array of cube textures to use in a shader-resource view. |
| [D3D12_TEXCUBE_SRV structure](..\d3d12\ns-d3d12-d3d12_texcube_srv.md) | Describes the subresource from a cube texture to use in a shader-resource view. |
| [D3D12_TEXTURE_COPY_LOCATION structure](..\d3d12\ns-d3d12-d3d12_texture_copy_location.md) | Describes a portion of a texture for the purpose of texture copies. |
| [D3D12_TILED_RESOURCE_COORDINATE structure](..\d3d12\ns-d3d12-d3d12_tiled_resource_coordinate.md) | Describes the coordinates of a tiled resource. |
| [D3D12_TILE_REGION_SIZE structure](..\d3d12\ns-d3d12-d3d12_tile_region_size.md) | Describes the size of a tiled region. |
| [D3D12_TILE_SHAPE structure](..\d3d12\ns-d3d12-d3d12_tile_shape.md) | Describes the shape of a tile by specifying its dimensions. |
| [D3D12_UNORDERED_ACCESS_VIEW_DESC structure](..\d3d12\ns-d3d12-d3d12_unordered_access_view_desc.md) | Describes the subresources from a resource that are accessible by using an unordered-access view. |
| [D3D12_VERSIONED_ROOT_SIGNATURE_DESC structure](..\d3d12\ns-d3d12-d3d12_versioned_root_signature_desc.md) | Holds any version of a root signature description, and is designed to be used with serialization/deserialization functions. |
| [D3D12_VERTEX_BUFFER_VIEW structure](..\d3d12\ns-d3d12-d3d12_vertex_buffer_view.md) | Describes a vertex buffer view. |
| [D3D12_VIEWPORT structure](..\d3d12\ns-d3d12-d3d12_viewport.md) | Describes the dimensions of a viewport. |
| [D3D12_VIEW_INSTANCE_LOCATION structure](..\d3d12\ns-d3d12-d3d12_view_instance_location.md) | Specifies the viewport/stencil and render target associated with a view instance. |
| [D3D12_VIEW_INSTANCING_DESC structure](..\d3d12\ns-d3d12-d3d12_view_instancing_desc.md) | Specifies parameters used during view instancing configuration. |
| [D3D12_WRITEBUFFERIMMEDIATE_PARAMETER structure](..\d3d12\ns-d3d12-d3d12_writebufferimmediate_parameter.md) | Specifies the immediate value and destination address written using ID3D12CommandList2 |
| [_D3D12_FUNCTION_DESC structure](..\d3d12shader\ns-d3d12shader-_d3d12_function_desc.md) | Describes a function. |
| [_D3D12_LIBRARY_DESC structure](..\d3d12shader\ns-d3d12shader-_d3d12_library_desc.md) | Describes a library. |
| [_D3D12_PARAMETER_DESC structure](..\d3d12shader\ns-d3d12shader-_d3d12_parameter_desc.md) | Describes a function parameter. |
| [_D3D12_SHADER_BUFFER_DESC structure](..\d3d12shader\ns-d3d12shader-_d3d12_shader_buffer_desc.md) | Describes a shader constant-buffer. |
| [_D3D12_SHADER_DESC structure](..\d3d12shader\ns-d3d12shader-_d3d12_shader_desc.md) | Describes a shader. |
| [_D3D12_SHADER_INPUT_BIND_DESC structure](..\d3d12shader\ns-d3d12shader-_d3d12_shader_input_bind_desc.md) | Describes how a shader resource is bound to a shader input. |
| [_D3D12_SHADER_TYPE_DESC structure](..\d3d12shader\ns-d3d12shader-_d3d12_shader_type_desc.md) | Describes a shader-variable type. |
| [_D3D12_SHADER_VARIABLE_DESC structure](..\d3d12shader\ns-d3d12shader-_d3d12_shader_variable_desc.md) | Describes a shader variable. |
| [_D3D12_SIGNATURE_PARAMETER_DESC structure](..\d3d12shader\ns-d3d12shader-_d3d12_signature_parameter_desc.md) | Describes a shader signature. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [D3D12_BLEND enumeration](..\d3d12\ne-d3d12-d3d12_blend.md) | Specifies blend factors, which modulate values for the pixel shader and render target. |
| [D3D12_BLEND_OP enumeration](..\d3d12\ne-d3d12-d3d12_blend_op.md) | Specifies RGB or alpha blending operations. |
| [D3D12_BUFFER_SRV_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_buffer_srv_flags.md) | Identifies how to view a buffer resource. |
| [D3D12_BUFFER_UAV_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_buffer_uav_flags.md) | Identifies unordered-access view options for a buffer resource. |
| [D3D12_CLEAR_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_clear_flags.md) | Specifies what to clear from the depth stencil view. |
| [D3D12_COLOR_WRITE_ENABLE enumeration](..\d3d12\ne-d3d12-d3d12_color_write_enable.md) | Identifies which components of each pixel of a render target are writable during blending. |
| [D3D12_COMMAND_LIST_SUPPORT_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_command_list_support_flags.md) | Used to determine which kinds of command lists are capable of supporting various operations. |
| [D3D12_COMMAND_LIST_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_command_list_type.md) | Specifies the type of a command list. |
| [D3D12_COMMAND_QUEUE_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_command_queue_flags.md) | Specifies flags to be used when creating a command queue. |
| [D3D12_COMMAND_QUEUE_PRIORITY enumeration](..\d3d12\ne-d3d12-d3d12_command_queue_priority.md) | Defines priority levels for a command queue. |
| [D3D12_COMPARISON_FUNC enumeration](..\d3d12\ne-d3d12-d3d12_comparison_func.md) | Specifies comparison options. |
| [D3D12_CONSERVATIVE_RASTERIZATION_MODE enumeration](..\d3d12\ne-d3d12-d3d12_conservative_rasterization_mode.md) | Identifies whether conservative rasterization is on or off. |
| [D3D12_CONSERVATIVE_RASTERIZATION_TIER enumeration](..\d3d12\ne-d3d12-d3d12_conservative_rasterization_tier.md) | Identifies the tier level of conservative rasterization. |
| [D3D12_CPU_PAGE_PROPERTY enumeration](..\d3d12\ne-d3d12-d3d12_cpu_page_property.md) | Specifies the CPU-page properties for the heap. |
| [D3D12_CROSS_NODE_SHARING_TIER enumeration](..\d3d12\ne-d3d12-d3d12_cross_node_sharing_tier.md) | Specifies the level of sharing across nodes of an adapter, such as Tier 1 Emulated, Tier 1, or Tier 2. |
| [D3D12_CULL_MODE enumeration](..\d3d12\ne-d3d12-d3d12_cull_mode.md) | Specifies triangles facing a particular direction are not drawn. |
| [D3D12_DEBUG_COMMAND_LIST_PARAMETER_TYPE enumeration](..\d3d12sdklayers\ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type.md) | Indicates the debug parameter type used by ID3D12DebugCommandList1 |
| [D3D12_DEBUG_DEVICE_PARAMETER_TYPE enumeration](..\d3d12sdklayers\ne-d3d12sdklayers-d3d12_debug_device_parameter_type.md) | Specifies the data type of the memory pointed to by the pData parameter of ID3D12DebugDevice1 |
| [D3D12_DEBUG_FEATURE enumeration](..\d3d12sdklayers\ne-d3d12sdklayers-d3d12_debug_feature.md) | Flags for optional D3D12 Debug Layer features. |
| [D3D12_DEPTH_WRITE_MASK enumeration](..\d3d12\ne-d3d12-d3d12_depth_write_mask.md) | Identifies the portion of a depth-stencil buffer for writing depth data. |
| [D3D12_DESCRIPTOR_HEAP_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_descriptor_heap_flags.md) | Specifies options for a heap. |
| [D3D12_DESCRIPTOR_HEAP_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_descriptor_heap_type.md) | Specifies a type of descriptor heap. |
| [D3D12_DESCRIPTOR_RANGE_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_descriptor_range_flags.md) | Specifies the volatility of both descriptors and the data they reference in a Root Signature 1.1 description, which can enable some driver optimizations. |
| [D3D12_DESCRIPTOR_RANGE_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_descriptor_range_type.md) | Specifies a range so that, for example, if part of a descriptor table has 100 shader-resource views (SRVs) that range can be declared in one entry rather than 100. |
| [D3D12_DSV_DIMENSION enumeration](..\d3d12\ne-d3d12-d3d12_dsv_dimension.md) | Specifies how to access a resource used in a depth-stencil view. |
| [D3D12_DSV_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_dsv_flags.md) | Specifies depth-stencil view options. |
| [D3D12_FEATURE enumeration](..\d3d12\ne-d3d12-d3d12_feature.md) | Direct3D 12 feature options that are supported by the current graphics driver. |
| [D3D12_FENCE_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_fence_flags.md) | Specifies fence options. |
| [D3D12_FILL_MODE enumeration](..\d3d12\ne-d3d12-d3d12_fill_mode.md) | Specifies the fill mode to use when rendering triangles. |
| [D3D12_FILTER enumeration](..\d3d12\ne-d3d12-d3d12_filter.md) | Specifies filtering options during texture sampling. |
| [D3D12_FILTER_REDUCTION_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_filter_reduction_type.md) | Specifies the type of filter reduction. |
| [D3D12_FILTER_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_filter_type.md) | Specifies the type of magnification or minification sampler filters. |
| [D3D12_FORMAT_SUPPORT1 enumeration](..\d3d12\ne-d3d12-d3d12_format_support1.md) | Specifies resources that are supported for a provided format. |
| [D3D12_FORMAT_SUPPORT2 enumeration](..\d3d12\ne-d3d12-d3d12_format_support2.md) | Specifies which unordered resource options are supported for a provided format. |
| [D3D12_GPU_BASED_VALIDATION_FLAGS enumeration](..\d3d12sdklayers\ne-d3d12sdklayers-d3d12_gpu_based_validation_flags.md) | Describes the level of GPU-based validation to perform at runtime. |
| [D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS enumeration](..\d3d12sdklayers\ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags.md) | Specifies how GPU-Based Validation handles patched pipeline states during ID3D12Device |
| [D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE enumeration](..\d3d12sdklayers\ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode.md) | Specifies the type of shader patching used by GPU-Based Validation at either the device or command list level. |
| [D3D12_HEAP_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_heap_flags.md) | Specifies heap options, such as whether the heap can contain textures, and whether resources are shared across adapters. |
| [D3D12_HEAP_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_heap_type.md) | Specifies the type of heap. When resident, heaps reside in a particular physical memory pool with certain CPU cache properties. |
| [D3D12_INDEX_BUFFER_STRIP_CUT_VALUE enumeration](..\d3d12\ne-d3d12-d3d12_index_buffer_strip_cut_value.md) | When using triangle strip primitive topology, vertex positions are interpreted as vertices of a continuous triangle “strip”. |
| [D3D12_INDIRECT_ARGUMENT_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_indirect_argument_type.md) | Specifies the type of the indirect parameter. |
| [D3D12_INPUT_CLASSIFICATION enumeration](..\d3d12\ne-d3d12-d3d12_input_classification.md) | Identifies the type of data contained in an input slot. |
| [D3D12_LOGIC_OP enumeration](..\d3d12\ne-d3d12-d3d12_logic_op.md) | Specifies logical operations to configure for a render target. |
| [D3D12_MEMORY_POOL enumeration](..\d3d12\ne-d3d12-d3d12_memory_pool.md) | Specifies the memory pool for the heap. |
| [D3D12_MESSAGE_CATEGORY enumeration](..\d3d12sdklayers\ne-d3d12sdklayers-d3d12_message_category.md) | Specifies categories of debug messages. |
| [D3D12_MESSAGE_ID enumeration](..\d3d12sdklayers\ne-d3d12sdklayers-d3d12_message_id.md) | Specifies debug message IDs for setting up an info-queue filter (see D3D12_INFO_QUEUE_FILTER); use these messages to allow or deny message categories to pass through the storage and retrieval filters. |
| [D3D12_MESSAGE_SEVERITY enumeration](..\d3d12sdklayers\ne-d3d12sdklayers-d3d12_message_severity.md) | Debug message severity levels for an information queue. |
| [D3D12_MULTIPLE_FENCE_WAIT_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_multiple_fence_wait_flags.md) | Specifies multiple wait flags for multiple fences. |
| [D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_multisample_quality_level_flags.md) | Specifies options for determining quality levels. |
| [D3D12_PIPELINE_STATE_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_pipeline_state_flags.md) | Flags to control pipeline state. |
| [D3D12_PIPELINE_STATE_SUBOBJECT_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_pipeline_state_subobject_type.md) | Specifies the type of a sub-object in a pipeline state stream description. |
| [D3D12_PREDICATION_OP enumeration](..\d3d12\ne-d3d12-d3d12_predication_op.md) | Specifies the predication operation to apply. |
| [D3D12_PRIMITIVE_TOPOLOGY_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_primitive_topology_type.md) | Specifies how the pipeline interprets geometry or hull shader input primitives. |
| [D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER enumeration](..\d3d12\ne-d3d12-d3d12_programmable_sample_positions_tier.md) | Specifies the level of support for programmable sample positions that's offered by the adapter. |
| [D3D12_QUERY_HEAP_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_query_heap_type.md) | Specifies the type of query heap to create. |
| [D3D12_QUERY_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_query_type.md) | Specifies the type of query. |
| [D3D12_RESIDENCY_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_residency_flags.md) | Used with the EnqueuMakeResident function to choose how residency operations proceed when the memory budget is exceeded. |
| [D3D12_RESIDENCY_PRIORITY enumeration](..\d3d12\ne-d3d12-d3d12_residency_priority.md) | Specifies broad residency priority buckets useful for quickly establishing an application priority scheme. |
| [D3D12_RESOLVE_MODE enumeration](..\d3d12\ne-d3d12-d3d12_resolve_mode.md) | Specifies a resolve operation. |
| [D3D12_RESOURCE_BARRIER_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_resource_barrier_flags.md) | Flags for setting split resource barriers. |
| [D3D12_RESOURCE_BARRIER_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_resource_barrier_type.md) | Specifies a type of resource barrier (transition in resource use) description. |
| [D3D12_RESOURCE_BINDING_TIER enumeration](..\d3d12\ne-d3d12-d3d12_resource_binding_tier.md) | Identifies the tier of resource binding being used. |
| [D3D12_RESOURCE_DIMENSION enumeration](..\d3d12\ne-d3d12-d3d12_resource_dimension.md) | Identifies the type of resource being used. |
| [D3D12_RESOURCE_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_resource_flags.md) | Specifies options for working with resources. |
| [D3D12_RESOURCE_HEAP_TIER enumeration](..\d3d12\ne-d3d12-d3d12_resource_heap_tier.md) | Specifies which resource heap tier the hardware and driver support. |
| [D3D12_RESOURCE_STATES enumeration](..\d3d12\ne-d3d12-d3d12_resource_states.md) | Specifies the state of a resource regarding how the resource is being used. |
| [D3D12_RLDO_FLAGS enumeration](..\d3d12sdklayers\ne-d3d12sdklayers-d3d12_rldo_flags.md) | Specifies options for the amount of information to report about a live device object's lifetime. |
| [D3D12_ROOT_DESCRIPTOR_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_root_descriptor_flags.md) | Specifies the volatility of the data referenced by descriptors in a Root Signature 1.1 description, which can enable some driver optimizations. |
| [D3D12_ROOT_PARAMETER_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_root_parameter_type.md) | Specifies the type of root signature slot. |
| [D3D12_ROOT_SIGNATURE_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_root_signature_flags.md) | Specifies options for root signature layout. |
| [D3D12_RTV_DIMENSION enumeration](..\d3d12\ne-d3d12-d3d12_rtv_dimension.md) | Identifies the type of resource to view as a render target. |
| [D3D12_SHADER_CACHE_SUPPORT_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_shader_cache_support_flags.md) | Describes the level of support for shader caching in the current graphics driver. |
| [D3D12_SHADER_COMPONENT_MAPPING enumeration](..\d3d12\ne-d3d12-d3d12_shader_component_mapping.md) | Specifies how memory gets routed by a shader resource view (SRV). |
| [D3D12_SHADER_MIN_PRECISION_SUPPORT enumeration](..\d3d12\ne-d3d12-d3d12_shader_min_precision_support.md) | Describes minimum precision support options for shaders in the current graphics driver. |
| [D3D12_SHADER_VERSION_TYPE enumeration](..\d3d12shader\ne-d3d12shader-d3d12_shader_version_type.md) | Enumerates the types of shaders that Direct3D recognizes. Used to encode the Version member of the D3D12_SHADER_DESC structure. |
| [D3D12_SHADER_VISIBILITY enumeration](..\d3d12\ne-d3d12-d3d12_shader_visibility.md) | Specifies the shaders that can access the contents of a given root signature slot. |
| [D3D12_SRV_DIMENSION enumeration](..\d3d12\ne-d3d12-d3d12_srv_dimension.md) | Identifies the type of resource that will be viewed as a shader resource. |
| [D3D12_STATIC_BORDER_COLOR enumeration](..\d3d12\ne-d3d12-d3d12_static_border_color.md) | Specifies the border color for a static sampler. |
| [D3D12_STENCIL_OP enumeration](..\d3d12\ne-d3d12-d3d12_stencil_op.md) | Identifies the stencil operations that can be performed during depth-stencil testing. |
| [D3D12_TEXTURE_ADDRESS_MODE enumeration](..\d3d12\ne-d3d12-d3d12_texture_address_mode.md) | Identifies a technique for resolving texture coordinates that are outside of the boundaries of a texture. |
| [D3D12_TEXTURE_COPY_TYPE enumeration](..\d3d12\ne-d3d12-d3d12_texture_copy_type.md) | Specifies what type of texture copy is to take place. |
| [D3D12_TEXTURE_LAYOUT enumeration](..\d3d12\ne-d3d12-d3d12_texture_layout.md) | Specifies texture layout options. |
| [D3D12_TILED_RESOURCES_TIER enumeration](..\d3d12\ne-d3d12-d3d12_tiled_resources_tier.md) | Identifies the tier level at which tiled resources are supported. |
| [D3D12_TILE_COPY_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_tile_copy_flags.md) | Specifies how to copy a tile. |
| [D3D12_TILE_MAPPING_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_tile_mapping_flags.md) | Specifies how to perform a tile-mapping operation. |
| [D3D12_TILE_RANGE_FLAGS enumeration](..\d3d12\ne-d3d12-d3d12_tile_range_flags.md) | Specifies a range of tile mappings. |
| [D3D12_UAV_DIMENSION enumeration](..\d3d12\ne-d3d12-d3d12_uav_dimension.md) | Identifies unordered-access view options. |
| [D3D12_VIEW_INSTANCING_TIER enumeration](..\d3d12\ne-d3d12-d3d12_view_instancing_tier.md) | Indicates the tier level at which view instancing is supported. |
| [D3D12_WRITEBUFFERIMMEDIATE_MODE enumeration](..\d3d12\ne-d3d12-d3d12_writebufferimmediate_mode.md) | Specifies the mode used by a WriteBufferImmediate operation. |
| [D3D_ROOT_SIGNATURE_VERSION enumeration](..\d3d12\ne-d3d12-d3d_root_signature_version.md) | Specifies the version of root signature layout. |
| [D3D_SHADER_MODEL enumeration](..\d3d12\ne-d3d12-d3d_shader_model.md) | Specifies a shader model. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [ID3D11On12Device interface](..\d3d11on12\nn-d3d11on12-id3d11on12device.md) | Handles the creation, wrapping and releasing of D3D11 resources for Direct3D 11on12. |
| [ID3D12CommandAllocator interface](..\d3d12\nn-d3d12-id3d12commandallocator.md) | Represents the allocations of storage for graphics processing unit (GPU) commands. |
| [ID3D12CommandList interface](..\d3d12\nn-d3d12-id3d12commandlist.md) | An interface from which ID3D12GraphicsCommandList inherits from. It represents an ordered set of commands that the GPU executes, while allowing for extension to support other command lists than just those for graphics (such as compute and copy). |
| [ID3D12CommandQueue interface](..\d3d12\nn-d3d12-id3d12commandqueue.md) | Provides methods for submitting command lists, synchronizing command list execution, instrumenting the command queue, and updating resource tile mappings. |
| [ID3D12Debug interface](..\d3d12sdklayers\nn-d3d12sdklayers-id3d12debug.md) | A debug interface controls debug settings and validates pipeline state. It can only be used if the debug layer is turned on. |
| [ID3D12Debug1 interface](..\d3d12sdklayers\nn-d3d12sdklayers-id3d12debug1.md) | Adds GPU-Based Validation and Dependent Command Queue Synchronization to the debug layer. |
| [ID3D12Debug2 interface](..\d3d12sdklayers\nn-d3d12sdklayers-id3d12debug2.md) | Adds configurable levels of GPU-Based Validation to the debug layer. |
| [ID3D12DebugCommandList interface](..\d3d12sdklayers\nn-d3d12sdklayers-id3d12debugcommandlist.md) | Provides methods to monitor and debug a command list. |
| [ID3D12DebugCommandList1 interface](..\d3d12sdklayers\nn-d3d12sdklayers-id3d12debugcommandlist1.md) | This interface enables modification of additional command list debug layer settings. |
| [ID3D12DebugCommandQueue interface](..\d3d12sdklayers\nn-d3d12sdklayers-id3d12debugcommandqueue.md) | Provides methods to monitor and debug a command queue. |
| [ID3D12DebugDevice interface](..\d3d12sdklayers\nn-d3d12sdklayers-id3d12debugdevice.md) | This interface represents a graphics device for debugging. |
| [ID3D12DebugDevice1 interface](..\d3d12sdklayers\nn-d3d12sdklayers-id3d12debugdevice1.md) | Specifies device-wide debug layer settings. |
| [ID3D12DescriptorHeap interface](..\d3d12\nn-d3d12-id3d12descriptorheap.md) | A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor. |
| [ID3D12Device interface](..\d3d12\nn-d3d12-id3d12device.md) | Represents a virtual adapter; it is used to create command allocators, command lists, command queues, fences, resources, pipeline state objects, heaps, root signatures, samplers, and many resource views. |
| [ID3D12Device1 interface](..\d3d12\nn-d3d12-id3d12device1.md) | Represents a virtual adapter, and expands on the range of methods provided by ID3D12Device. |
| [ID3D12Device2 interface](..\d3d12\nn-d3d12-id3d12device2.md) | Represents a virtual adapter. This interface extends ID3D12Device1 to create pipeline state objects from pipeline state stream descriptions. |
| [ID3D12Device3 interface](..\d3d12\nn-d3d12-id3d12device3.md) | Represents a virtual adapter. This interface extends Id3d12device2 to support the creation of special-purpose diagnostic heaps in system memory that persist even in the event of a GPU-fault or device-removed scenario. |
| [ID3D12DeviceChild interface](..\d3d12\nn-d3d12-id3d12devicechild.md) | An interface from which other core interfaces inherit from, including ID3D12PipelineLibrary, ID3D12CommandList, ID3D12Pageable, and ID3D12RootSignature. It provides a method to get back to the device object it was created against. |
| [ID3D12Fence interface](..\d3d12\nn-d3d12-id3d12fence.md) | Represents a fence, an object used for synchronization of the CPU and one or more GPUs. |
| [ID3D12Fence1 interface](..\d3d12\nn-d3d12-id3d12fence1.md) | Represents a fence. This interface extends ID3D12Fence, and supports the retrieval of the flags used to create the original fence. |
| [ID3D12FunctionParameterReflection interface](..\d3d12shader\nn-d3d12shader-id3d12functionparameterreflection.md) | A function-parameter-reflection interface accesses function-parameter info. |
| [ID3D12FunctionReflection interface](..\d3d12shader\nn-d3d12shader-id3d12functionreflection.md) | A function-reflection interface accesses function info. |
| [ID3D12GraphicsCommandList interface](..\d3d12\nn-d3d12-id3d12graphicscommandlist.md) | Encapsulates a list of graphics commands for rendering. Includes APIs for instrumenting the command list execution, and for setting and clearing the pipeline state. |
| [ID3D12GraphicsCommandList1 interface](..\d3d12\nn-d3d12-id3d12graphicscommandlist1.md) | Encapsulates a list of graphics commands for rendering, extending the inteface to support programmable sample positions, atomic copies for implementing late-latch techniques, and optional depth-bounds testing. |
| [ID3D12GraphicsCommandList2 interface](..\d3d12\nn-d3d12-id3d12graphicscommandlist2.md) | Encapsulates a list of graphics commands for rendering, extending the interface to support writing immediate values directly to a buffer. |
| [ID3D12Heap interface](..\d3d12\nn-d3d12-id3d12heap.md) | A heap is an abstraction of contiguous memory allocation, used to manage physical memory. This heap can be used with ID3D12Resource objects to support placed resources or reserved resources. |
| [ID3D12InfoQueue interface](..\d3d12sdklayers\nn-d3d12sdklayers-id3d12infoqueue.md) | An information-queue interface stores, retrieves, and filters debug messages. The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack. |
| [ID3D12LibraryReflection interface](..\d3d12shader\nn-d3d12shader-id3d12libraryreflection.md) | A library-reflection interface accesses library info. |
| [ID3D12Object interface](..\d3d12\nn-d3d12-id3d12object.md) | An interface from which ID3D12Device and ID3D12DeviceChild inherit from. It provides methods to associate private data and annotate object names. |
| [ID3D12PipelineLibrary interface](..\d3d12\nn-d3d12-id3d12pipelinelibrary.md) | Manages a pipeline library, in particular loading and retrieving individual PSOs. |
| [ID3D12PipelineLibrary1 interface](..\d3d12\nn-d3d12-id3d12pipelinelibrary1.md) | Manages a pipeline library. This interface extends ID3D12PipelineLibrary to load PSOs from a pipeline state stream description. |
| [ID3D12PipelineState interface](..\d3d12\nn-d3d12-id3d12pipelinestate.md) | Represents the state of all currently set shaders as well as certain fixed function state objects. |
| [ID3D12Resource interface](..\d3d12\nn-d3d12-id3d12resource.md) | Encapsulates a generalized ability of the CPU and GPU to read and write to physical memory, or heaps. It contains abstractions for organizing and manipulating simple arrays of data as well as multidimensional data optimized for shader sampling. |
| [ID3D12RootSignatureDeserializer interface](..\d3d12\nn-d3d12-id3d12rootsignaturedeserializer.md) | Contains a method to return the deserialized D3D12_ROOT_SIGNATURE_DESC data structure, of a serialized root signature version 1.0. |
| [ID3D12ShaderReflection interface](..\d3d12shader\nn-d3d12shader-id3d12shaderreflection.md) | A shader-reflection interface accesses shader information. |
| [ID3D12ShaderReflectionConstantBuffer interface](..\d3d12shader\nn-d3d12shader-id3d12shaderreflectionconstantbuffer.md) | This shader-reflection interface provides access to a constant buffer. |
| [ID3D12ShaderReflectionType interface](..\d3d12shader\nn-d3d12shader-id3d12shaderreflectiontype.md) | This shader-reflection interface provides access to variable type. |
| [ID3D12ShaderReflectionVariable interface](..\d3d12shader\nn-d3d12shader-id3d12shaderreflectionvariable.md) | This shader-reflection interface provides access to a variable. |
| [ID3D12SharingContract interface](..\d3d12sdklayers\nn-d3d12sdklayers-id3d12sharingcontract.md) | Part of a contract between D3D11On12 diagnostic layers and graphics diagnostics tools. |
| [ID3D12Tools interface](..\d3d12\nn-d3d12-id3d12tools.md) | This interface is used to configure the runtime for tools such as PIX. Its not intended or supported for any other scenario. |
| [ID3D12VersionedRootSignatureDeserializer interface](..\d3d12\nn-d3d12-id3d12versionedrootsignaturedeserializer.md) | Contains methods to return the deserialized D3D12_ROOT_SIGNATURE_DESC1 data structure, of any version of a serialized root signature. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [ID3D11On12Device::AcquireWrappedResources](..\d3d11on12\nf-d3d11on12-id3d11on12device-acquirewrappedresources.md) | Acquires D3D11 resources for use with D3D 11on12. Indicates that rendering to the wrapped resources can begin again. |
| [ID3D11On12Device::CreateWrappedResource](..\d3d11on12\nf-d3d11on12-id3d11on12device-createwrappedresource.md) | This method creates D3D11 resources for use with D3D 11on12. |
| [ID3D11On12Device::ReleaseWrappedResources](..\d3d11on12\nf-d3d11on12-id3d11on12device-releasewrappedresources.md) | Releases D3D11 resources that were wrapped for D3D 11on12. |
| [ID3D12CommandAllocator::Reset](..\d3d12\nf-d3d12-id3d12commandallocator-reset.md) | Indicates to re-use the memory that is associated with the command allocator. |
| [ID3D12CommandList::GetType](..\d3d12\nf-d3d12-id3d12commandlist-gettype.md) | Gets the type of the command list, such as direct, bundle, compute, or copy. |
| [ID3D12CommandQueue::BeginEvent](..\d3d12\nf-d3d12-id3d12commandqueue-beginevent.md) | Not intended to be called directly.  Use the PIX event runtime to insert events into a command queue. |
| [ID3D12CommandQueue::CopyTileMappings](..\d3d12\nf-d3d12-id3d12commandqueue-copytilemappings.md) | Copies mappings from a source reserved resource to a destination reserved resource. |
| [ID3D12CommandQueue::EndEvent](..\d3d12\nf-d3d12-id3d12commandqueue-endevent.md) | Not intended to be called directly.  Use the PIX event runtime to insert events into a command queue. |
| [ID3D12CommandQueue::ExecuteCommandLists](..\d3d12\nf-d3d12-id3d12commandqueue-executecommandlists.md) | Submits an array of command lists for execution. |
| [ID3D12CommandQueue::GetClockCalibration](..\d3d12\nf-d3d12-id3d12commandqueue-getclockcalibration.md) | This method samples the CPU and GPU timestamp counters at the same moment in time. |
| [ID3D12CommandQueue::GetDesc](..\d3d12\nf-d3d12-id3d12commandqueue-getdesc.md) | Gets the description of the command queue. |
| [ID3D12CommandQueue::GetTimestampFrequency](..\d3d12\nf-d3d12-id3d12commandqueue-gettimestampfrequency.md) | This method is used to determine the rate at which the GPU timestamp counter increments. |
| [ID3D12CommandQueue::SetMarker](..\d3d12\nf-d3d12-id3d12commandqueue-setmarker.md) | Not intended to be called directly.  Use the PIX event runtime to insert events into a command queue. |
| [ID3D12CommandQueue::Signal](..\d3d12\nf-d3d12-id3d12commandqueue-signal.md) | Updates a fence to a specified value. |
| [ID3D12CommandQueue::UpdateTileMappings](..\d3d12\nf-d3d12-id3d12commandqueue-updatetilemappings.md) | Updates mappings of tile locations in reserved resources to memory locations in a resource heap. |
| [ID3D12CommandQueue::Wait](..\d3d12\nf-d3d12-id3d12commandqueue-wait.md) | Waits until the specified fence reaches or exceeds the specified value. |
| [ID3D12Debug1::EnableDebugLayer](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debug1-enabledebuglayer.md) | Enables the debug layer. |
| [ID3D12Debug1::SetEnableGPUBasedValidation](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation.md) | This method enables or disables GPU-Based Validation (GBV) before creating a device with the debug layer enabled. |
| [ID3D12Debug1::SetEnableSynchronizedCommandQueueValidation](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debug1-setenablesynchronizedcommandqueuevalidation.md) | Enables or disables dependent command queue synchronization when using a D3D12 device with the debug layer enabled. |
| [ID3D12Debug2::SetGPUBasedValidationFlags](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debug2-setgpubasedvalidationflags.md) | This method configures the level of GPU-based validation that the debug device is to perform at runtime. |
| [ID3D12Debug::EnableDebugLayer](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debug-enabledebuglayer.md) | Enables the debug layer. |
| [ID3D12DebugCommandList1::AssertResourceState](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugcommandlist1-assertresourcestate.md) | Validates that the given state matches the state of the subresource, assuming the state of the given subresource is known during recording of a command list (e.g. |
| [ID3D12DebugCommandList1::GetDebugParameter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugcommandlist1-getdebugparameter.md) | Gets optional Command List Debug Layer settings. |
| [ID3D12DebugCommandList1::SetDebugParameter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugcommandlist1-setdebugparameter.md) | Modifies optional Debug Layer settings of a command list. |
| [ID3D12DebugCommandList::AssertResourceState](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugcommandlist-assertresourcestate.md) | Checks whether a resource, or subresource, is in a specified state, or not. |
| [ID3D12DebugCommandList::GetFeatureMask](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugcommandlist-getfeaturemask.md) | Returns the debug feature flags that have been set on a command list. |
| [ID3D12DebugCommandList::SetFeatureMask](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugcommandlist-setfeaturemask.md) | Turns the debug features for a command list on or off. |
| [ID3D12DebugCommandQueue::AssertResourceState](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugcommandqueue-assertresourcestate.md) | Checks whether a resource, or subresource, is in a specified state, or not. |
| [ID3D12DebugDevice1::GetDebugParameter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugdevice1-getdebugparameter.md) | Gets optional device-wide Debug Layer settings. |
| [ID3D12DebugDevice1::ReportLiveDeviceObjects](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugdevice1-reportlivedeviceobjects.md) | Specifies the amount of information to report on a device object's lifetime. |
| [ID3D12DebugDevice1::SetDebugParameter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter.md) | Modifies the D3D12 optional device-wide Debug Layer settings. |
| [ID3D12DebugDevice::GetFeatureMask](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugdevice-getfeaturemask.md) | Gets a bit field of flags that indicates which debug features are on or off. |
| [ID3D12DebugDevice::ReportLiveDeviceObjects](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugdevice-reportlivedeviceobjects.md) | Reports information about a device object's lifetime. |
| [ID3D12DebugDevice::SetFeatureMask](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12debugdevice-setfeaturemask.md) | Set a bit field of flags that will turn debug features on and off. |
| [ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart](..\d3d12\nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart.md) | Gets the CPU descriptor handle that represents the start of the heap. |
| [ID3D12DescriptorHeap::GetDesc](..\d3d12\nf-d3d12-id3d12descriptorheap-getdesc.md) | Gets the descriptor heap description. |
| [ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart](..\d3d12\nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart.md) | Gets the GPU descriptor handle that represents the start of the heap. |
| [ID3D12Device1::CreatePipelineLibrary](..\d3d12\nf-d3d12-id3d12device1-createpipelinelibrary.md) | Creates a cached pipeline library. |
| [ID3D12Device1::SetEventOnMultipleFenceCompletion](..\d3d12\nf-d3d12-id3d12device1-seteventonmultiplefencecompletion.md) | Specifies an event that should be fired when one or more of a collection of fences reach specific values. |
| [ID3D12Device1::SetResidencyPriority](..\d3d12\nf-d3d12-id3d12device1-setresidencypriority.md) | This method sets residency priorities of a specified list of objects. |
| [ID3D12Device2::CreatePipelineState](..\d3d12\nf-d3d12-id3d12device2-createpipelinestate.md) | Creates a pipeline state object from a pipeline state stream description. |
| [ID3D12Device3::EnqueueMakeResident](..\d3d12\nf-d3d12-id3d12device3-enqueuemakeresident.md) | Asynchronously makes objects resident for the device. |
| [ID3D12Device3::OpenExistingHeapFromAddress](..\d3d12\nf-d3d12-id3d12device3-openexistingheapfromaddress.md) | Creates a special-purpose diagnostic heap in system memory from an address. The created heap can persist even in the event of a GPU-fault or device-removed scenario. |
| [ID3D12Device::CheckFeatureSupport](..\d3d12\nf-d3d12-id3d12device-checkfeaturesupport.md) | Gets information about the features that are supported by the current graphics driver. |
| [ID3D12Device::CopyDescriptorsSimple](..\d3d12\nf-d3d12-id3d12device-copydescriptorssimple.md) | Copies descriptors from a source to a destination. |
| [ID3D12Device::CopyDescriptors](..\d3d12\nf-d3d12-id3d12device-copydescriptors.md) | Copies descriptors from a source to a destination. |
| [ID3D12Device::CreateCommandAllocator](..\d3d12\nf-d3d12-id3d12device-createcommandallocator.md) | Creates a command allocator object. |
| [ID3D12Device::CreateCommandList](..\d3d12\nf-d3d12-id3d12device-createcommandlist.md) | Creates a command list. |
| [ID3D12Device::CreateCommandQueue](..\d3d12\nf-d3d12-id3d12device-createcommandqueue.md) | Creates a command queue. |
| [ID3D12Device::CreateCommandSignature](..\d3d12\nf-d3d12-id3d12device-createcommandsignature.md) | This method creates a command signature. |
| [ID3D12Device::CreateCommittedResource](..\d3d12\nf-d3d12-id3d12device-createcommittedresource.md) | Creates both a resource and an implicit heap, such that the heap is big enough to contain the entire resource and the resource is mapped to the heap. |
| [ID3D12Device::CreateComputePipelineState](..\d3d12\nf-d3d12-id3d12device-createcomputepipelinestate.md) | Creates a compute pipeline state object. |
| [ID3D12Device::CreateConstantBufferView](..\d3d12\nf-d3d12-id3d12device-createconstantbufferview.md) | Creates a constant-buffer view for accessing resource data. |
| [ID3D12Device::CreateDepthStencilView](..\d3d12\nf-d3d12-id3d12device-createdepthstencilview.md) | Creates a depth-stencil view for accessing resource data. |
| [ID3D12Device::CreateDescriptorHeap](..\d3d12\nf-d3d12-id3d12device-createdescriptorheap.md) | Creates a descriptor heap object. |
| [ID3D12Device::CreateFence](..\d3d12\nf-d3d12-id3d12device-createfence.md) | Creates a fence object. |
| [ID3D12Device::CreateGraphicsPipelineState](..\d3d12\nf-d3d12-id3d12device-creategraphicspipelinestate.md) | Creates a graphics pipeline state object. |
| [ID3D12Device::CreateHeap](..\d3d12\nf-d3d12-id3d12device-createheap.md) | Creates a heap that can be used with placed resources and reserved resources. |
| [ID3D12Device::CreatePlacedResource](..\d3d12\nf-d3d12-id3d12device-createplacedresource.md) | Creates a resource that is placed in a specific heap. Placed resources are the lightest weight resource objects available, and are the fastest to create and destroy. |
| [ID3D12Device::CreateQueryHeap](..\d3d12\nf-d3d12-id3d12device-createqueryheap.md) | Creates a query heap. A query heap contains an array of queries. |
| [ID3D12Device::CreateRenderTargetView](..\d3d12\nf-d3d12-id3d12device-createrendertargetview.md) | Creates a render-target view for accessing resource data. |
| [ID3D12Device::CreateReservedResource](..\d3d12\nf-d3d12-id3d12device-createreservedresource.md) | Creates a resource that is reserved, which is not yet mapped to any pages in a heap. |
| [ID3D12Device::CreateRootSignature](..\d3d12\nf-d3d12-id3d12device-createrootsignature.md) | Creates a root signature layout. |
| [ID3D12Device::CreateSampler](..\d3d12\nf-d3d12-id3d12device-createsampler.md) | Create a sampler object that encapsulates sampling information for a texture. |
| [ID3D12Device::CreateShaderResourceView](..\d3d12\nf-d3d12-id3d12device-createshaderresourceview.md) | Creates a shader-resource view for accessing data in a resource. |
| [ID3D12Device::CreateSharedHandle](..\d3d12\nf-d3d12-id3d12device-createsharedhandle.md) | Creates a shared handle to an heap, resource, or fence object. |
| [ID3D12Device::CreateUnorderedAccessView](..\d3d12\nf-d3d12-id3d12device-createunorderedaccessview.md) | Creates a view for unordered accessing. |
| [ID3D12Device::Evict](..\d3d12\nf-d3d12-id3d12device-evict.md) | Enables the page-out of data, which precludes GPU access of that data. |
| [ID3D12Device::GetAdapterLuid](..\d3d12\nf-d3d12-id3d12device-getadapterluid.md) | Gets a locally unique identifier for the current device (adapter). |
| [ID3D12Device::GetCopyableFootprints](..\d3d12\nf-d3d12-id3d12device-getcopyablefootprints.md) | Gets a resource layout that can be copied. Helps the app fill-in D3D12_PLACED_SUBRESOURCE_FOOTPRINT and D3D12_SUBRESOURCE_FOOTPRINT when suballocating space in upload heaps. |
| [ID3D12Device::GetCustomHeapProperties](..\d3d12\nf-d3d12-id3d12device-getcustomheapproperties.md) | Divulges the equivalent custom heap properties that are used for non-custom heap types, based on the adapter's architectural properties. |
| [ID3D12Device::GetDescriptorHandleIncrementSize](..\d3d12\nf-d3d12-id3d12device-getdescriptorhandleincrementsize.md) | Gets the size of the handle increment for the given type of descriptor heap. This value is typically used to increment a handle into a descriptor array by the correct amount. |
| [ID3D12Device::GetDeviceRemovedReason](..\d3d12\nf-d3d12-id3d12device-getdeviceremovedreason.md) | Gets the reason that the device was removed. |
| [ID3D12Device::GetNodeCount](..\d3d12\nf-d3d12-id3d12device-getnodecount.md) | Reports the number of physical adapters (nodes) that are associated with this device. |
| [ID3D12Device::GetResourceAllocationInfo](..\d3d12\nf-d3d12-id3d12device-getresourceallocationinfo.md) | Gets the size and alignment of memory required for a collection of resources on this adapter. |
| [ID3D12Device::GetResourceTiling](..\d3d12\nf-d3d12-id3d12device-getresourcetiling.md) | Gets info about how a tiled resource is broken into tiles. |
| [ID3D12Device::MakeResident](..\d3d12\nf-d3d12-id3d12device-makeresident.md) | Makes objects resident for the device. |
| [ID3D12Device::OpenSharedHandleByName](..\d3d12\nf-d3d12-id3d12device-opensharedhandlebyname.md) | Opens a handle for shared resources, shared heaps, and shared fences, by using Name and Access. |
| [ID3D12Device::OpenSharedHandle](..\d3d12\nf-d3d12-id3d12device-opensharedhandle.md) | Opens a handle for shared resources, shared heaps, and shared fences, by using HANDLE and REFIID. |
| [ID3D12Device::SetStablePowerState](..\d3d12\nf-d3d12-id3d12device-setstablepowerstate.md) | A development-time aid for certain types of profiling and experimental prototyping. |
| [ID3D12DeviceChild::GetDevice](..\d3d12\nf-d3d12-id3d12devicechild-getdevice.md) | Gets a pointer to the device that created this interface. |
| [ID3D12Fence1::GetCreationFlags](..\d3d12\nf-d3d12-id3d12fence1-getcreationflags.md) | Gets the flags used to create the fence represented by the current instance. |
| [ID3D12Fence::GetCompletedValue](..\d3d12\nf-d3d12-id3d12fence-getcompletedvalue.md) | Gets the current value of the fence. |
| [ID3D12Fence::SetEventOnCompletion](..\d3d12\nf-d3d12-id3d12fence-seteventoncompletion.md) | Specifies an event that should be fired when the fence reaches a certain value. |
| [ID3D12Fence::Signal](..\d3d12\nf-d3d12-id3d12fence-signal.md) | Sets the fence to the specified value. |
| [ID3D12FunctionParameterReflection::GetDesc](..\d3d12shader\nf-d3d12shader-id3d12functionparameterreflection-getdesc.md) | Fills the parameter descriptor structure for the function's parameter. |
| [ID3D12FunctionReflection::GetConstantBufferByIndex](..\d3d12shader\nf-d3d12shader-id3d12functionreflection-getconstantbufferbyindex.md) | Gets a constant buffer by index for a function. |
| [ID3D12FunctionReflection::GetConstantBufferByName](..\d3d12shader\nf-d3d12shader-id3d12functionreflection-getconstantbufferbyname.md) | Gets a constant buffer by name for a function. |
| [ID3D12FunctionReflection::GetDesc](..\d3d12shader\nf-d3d12shader-id3d12functionreflection-getdesc.md) | Fills the function descriptor structure for the function. |
| [ID3D12FunctionReflection::GetFunctionParameter](..\d3d12shader\nf-d3d12shader-id3d12functionreflection-getfunctionparameter.md) | Gets the function parameter reflector. |
| [ID3D12FunctionReflection::GetResourceBindingDescByName](..\d3d12shader\nf-d3d12shader-id3d12functionreflection-getresourcebindingdescbyname.md) | Gets a description of how a resource is bound to a function. |
| [ID3D12FunctionReflection::GetResourceBindingDesc](..\d3d12shader\nf-d3d12shader-id3d12functionreflection-getresourcebindingdesc.md) | Gets a description of how a resource is bound to a function. |
| [ID3D12FunctionReflection::GetVariableByName](..\d3d12shader\nf-d3d12shader-id3d12functionreflection-getvariablebyname.md) | Gets a variable by name. |
| [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64](..\d3d12\nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64.md) | Atomically copies a primary data element of type UINT64 from one resource to another, along with optional dependent resources. |
| [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT](..\d3d12\nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint.md) | Atomically copies a primary data element of type UINT from one resource to another, along with optional dependent resources. |
| [ID3D12GraphicsCommandList1::OMSetDepthBounds](..\d3d12\nf-d3d12-id3d12graphicscommandlist1-omsetdepthbounds.md) | This method enables you to change the depth bounds dynamically. |
| [ID3D12GraphicsCommandList1::ResolveSubresourceRegion](..\d3d12\nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion.md) | Copy a region of a multisampled or compressed resource into a non-multisampled or non-compressed resource. |
| [ID3D12GraphicsCommandList1::SetSamplePositions](..\d3d12\nf-d3d12-id3d12graphicscommandlist1-setsamplepositions.md) | This method configures the sample positions used by subsequent draw, copy, resolve, and similar operations. |
| [ID3D12GraphicsCommandList1::SetViewInstanceMask](..\d3d12\nf-d3d12-id3d12graphicscommandlist1-setviewinstancemask.md) | Set a mask that controls which view instances are enabled for subsequent draws. |
| [ID3D12GraphicsCommandList2::WriteBufferImmediate](..\d3d12\nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate.md) | Writes a number of 32-bit immediate values to the specified buffer locations directly from the command stream. |
| [ID3D12GraphicsCommandList::BeginEvent](..\d3d12\nf-d3d12-id3d12graphicscommandlist-beginevent.md) | Not intended to be called directly.  Use the PIX event runtime to insert events into a command list. |
| [ID3D12GraphicsCommandList::BeginQuery](..\d3d12\nf-d3d12-id3d12graphicscommandlist-beginquery.md) | Starts a query running. |
| [ID3D12GraphicsCommandList::ClearDepthStencilView](..\d3d12\nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview.md) | Clears the depth-stencil resource. |
| [ID3D12GraphicsCommandList::ClearRenderTargetView](..\d3d12\nf-d3d12-id3d12graphicscommandlist-clearrendertargetview.md) | Sets all the elements in a render target to one value. |
| [ID3D12GraphicsCommandList::ClearState](..\d3d12\nf-d3d12-id3d12graphicscommandlist-clearstate.md) | Resets the state of a direct command list back to the state it was in when the command list was created. |
| [ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat](..\d3d12\nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat.md) | Sets all the elements in a unordered access view to the specified float values. |
| [ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint](..\d3d12\nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint.md) | Sets all the elements in a unordered-access view to the specified integer values. |
| [ID3D12GraphicsCommandList::Close](..\d3d12\nf-d3d12-id3d12graphicscommandlist-close.md) | Indicates that recording to the command list has finished. |
| [ID3D12GraphicsCommandList::CopyBufferRegion](..\d3d12\nf-d3d12-id3d12graphicscommandlist-copybufferregion.md) | Copies a region of a buffer from one resource to another. |
| [ID3D12GraphicsCommandList::CopyResource](..\d3d12\nf-d3d12-id3d12graphicscommandlist-copyresource.md) | Copies the entire contents of the source resource to the destination resource. |
| [ID3D12GraphicsCommandList::CopyTextureRegion](..\d3d12\nf-d3d12-id3d12graphicscommandlist-copytextureregion.md) | This method uses the GPU to copy texture data between two locations. Both the source and the destination may reference texture data located within either a buffer resource or a texture resource. |
| [ID3D12GraphicsCommandList::CopyTiles](..\d3d12\nf-d3d12-id3d12graphicscommandlist-copytiles.md) | Copies tiles from buffer to tiled resource or vice versa. |
| [ID3D12GraphicsCommandList::DiscardResource](..\d3d12\nf-d3d12-id3d12graphicscommandlist-discardresource.md) | Discards a resource. |
| [ID3D12GraphicsCommandList::Dispatch](..\d3d12\nf-d3d12-id3d12graphicscommandlist-dispatch.md) | Executes a command list from a thread group. |
| [ID3D12GraphicsCommandList::DrawIndexedInstanced](..\d3d12\nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced.md) | Draws indexed, instanced primitives. |
| [ID3D12GraphicsCommandList::DrawInstanced](..\d3d12\nf-d3d12-id3d12graphicscommandlist-drawinstanced.md) | Draws non-indexed, instanced primitives. |
| [ID3D12GraphicsCommandList::EndEvent](..\d3d12\nf-d3d12-id3d12graphicscommandlist-endevent.md) | Not intended to be called directly.  Use the PIX event runtime to insert events into a command list. |
| [ID3D12GraphicsCommandList::EndQuery](..\d3d12\nf-d3d12-id3d12graphicscommandlist-endquery.md) | Ends a running query. |
| [ID3D12GraphicsCommandList::ExecuteBundle](..\d3d12\nf-d3d12-id3d12graphicscommandlist-executebundle.md) | Executes a bundle. |
| [ID3D12GraphicsCommandList::ExecuteIndirect](..\d3d12\nf-d3d12-id3d12graphicscommandlist-executeindirect.md) | Apps perform indirect draws/dispatches using the ExecuteIndirect method. |
| [ID3D12GraphicsCommandList::IASetIndexBuffer](..\d3d12\nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer.md) | Sets the view for the index buffer. |
| [ID3D12GraphicsCommandList::IASetPrimitiveTopology](..\d3d12\nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology.md) | Bind information about the primitive type, and data order that describes input data for the input assembler stage. |
| [ID3D12GraphicsCommandList::IASetVertexBuffers](..\d3d12\nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers.md) | Sets a CPU descriptor handle for the vertex buffers. |
| [ID3D12GraphicsCommandList::OMSetBlendFactor](..\d3d12\nf-d3d12-id3d12graphicscommandlist-omsetblendfactor.md) | Sets the blend factor that modulate values for a pixel shader, render target, or both. |
| [ID3D12GraphicsCommandList::OMSetRenderTargets](..\d3d12\nf-d3d12-id3d12graphicscommandlist-omsetrendertargets.md) | Sets CPU descriptor handles for the render targets and depth stencil. |
| [ID3D12GraphicsCommandList::OMSetStencilRef](..\d3d12\nf-d3d12-id3d12graphicscommandlist-omsetstencilref.md) | Sets the reference value for depth stencil tests. |
| [ID3D12GraphicsCommandList::RSSetScissorRects](..\d3d12\nf-d3d12-id3d12graphicscommandlist-rssetscissorrects.md) | Binds an array of scissor rectangles to the rasterizer stage. |
| [ID3D12GraphicsCommandList::RSSetViewports](..\d3d12\nf-d3d12-id3d12graphicscommandlist-rssetviewports.md) | Bind an array of viewports to the rasterizer stage of the pipeline. |
| [ID3D12GraphicsCommandList::Reset](..\d3d12\nf-d3d12-id3d12graphicscommandlist-reset.md) | Resets a command list back to its initial state as if a new command list was just created. |
| [ID3D12GraphicsCommandList::ResolveQueryData](..\d3d12\nf-d3d12-id3d12graphicscommandlist-resolvequerydata.md) | Extracts data from a query. ResolveQueryData works with all heap types (default, upload, and readback).  ResolveQueryData works with all heap types (default, upload, and readback). . |
| [ID3D12GraphicsCommandList::ResolveSubresource](..\d3d12\nf-d3d12-id3d12graphicscommandlist-resolvesubresource.md) | Copy a multi-sampled resource into a non-multi-sampled resource. |
| [ID3D12GraphicsCommandList::ResourceBarrier](..\d3d12\nf-d3d12-id3d12graphicscommandlist-resourcebarrier.md) | Notifies the driver that it needs to synchronize multiple accesses to resources. |
| [ID3D12GraphicsCommandList::SOSetTargets](..\d3d12\nf-d3d12-id3d12graphicscommandlist-sosettargets.md) | Sets the stream output buffer views. |
| [ID3D12GraphicsCommandList::SetComputeRoot32BitConstant](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant.md) | Sets a constant in the compute root signature. |
| [ID3D12GraphicsCommandList::SetComputeRoot32BitConstants](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants.md) | Sets a group of constants in the compute root signature. |
| [ID3D12GraphicsCommandList::SetComputeRootConstantBufferView](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview.md) | Sets a CPU descriptor handle for the constant buffer in the compute root signature. |
| [ID3D12GraphicsCommandList::SetComputeRootDescriptorTable](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable.md) | Sets a descriptor table into the compute root signature. |
| [ID3D12GraphicsCommandList::SetComputeRootShaderResourceView](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview.md) | Sets a CPU descriptor handle for the shader resource in the compute root signature. |
| [ID3D12GraphicsCommandList::SetComputeRootSignature](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature.md) | Sets the layout of the compute root signature. |
| [ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview.md) | Sets a CPU descriptor handle for the unordered-access-view resource in the compute root signature. |
| [ID3D12GraphicsCommandList::SetDescriptorHeaps](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps.md) | Changes the currently bound descriptor heaps that are associated with a command list. |
| [ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstant](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant.md) | Sets a constant in the graphics root signature. |
| [ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstants](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants.md) | Sets a group of constants in the graphics root signature. |
| [ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview.md) | Sets a CPU descriptor handle for the constant buffer in the graphics root signature. |
| [ID3D12GraphicsCommandList::SetGraphicsRootDescriptorTable](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable.md) | Sets a descriptor table into the graphics root signature. |
| [ID3D12GraphicsCommandList::SetGraphicsRootShaderResourceView](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview.md) | Sets a CPU descriptor handle for the shader resource in the graphics root signature. |
| [ID3D12GraphicsCommandList::SetGraphicsRootSignature](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature.md) | Sets the layout of the graphics root signature. |
| [ID3D12GraphicsCommandList::SetGraphicsRootUnorderedAccessView](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview.md) | Sets a CPU descriptor handle for the unordered-access-view resource in the graphics root signature. |
| [ID3D12GraphicsCommandList::SetMarker](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setmarker.md) | Not intended to be called directly.  Use the PIX event runtime to insert events into a command list. |
| [ID3D12GraphicsCommandList::SetPipelineState](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setpipelinestate.md) | Sets all shaders and programs most of the fixed-function state of the graphics processing unit (GPU) pipeline. |
| [ID3D12GraphicsCommandList::SetPredication](..\d3d12\nf-d3d12-id3d12graphicscommandlist-setpredication.md) | Sets a rendering predicate. |
| [ID3D12InfoQueue::AddApplicationMessage](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-addapplicationmessage.md) | Adds a user-defined message to the message queue and sends that message to debug output. |
| [ID3D12InfoQueue::AddMessage](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-addmessage.md) | Adds a debug message to the message queue and sends that message to debug output. |
| [ID3D12InfoQueue::AddRetrievalFilterEntries](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-addretrievalfilterentries.md) | Add storage filters to the top of the retrieval-filter stack. |
| [ID3D12InfoQueue::AddStorageFilterEntries](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-addstoragefilterentries.md) | Add storage filters to the top of the storage-filter stack. |
| [ID3D12InfoQueue::ClearRetrievalFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-clearretrievalfilter.md) | Remove a retrieval filter from the top of the retrieval-filter stack. |
| [ID3D12InfoQueue::ClearStorageFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-clearstoragefilter.md) | Remove a storage filter from the top of the storage-filter stack. |
| [ID3D12InfoQueue::ClearStoredMessages](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-clearstoredmessages.md) | Clear all messages from the message queue. |
| [ID3D12InfoQueue::GetBreakOnCategory](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getbreakoncategory.md) | Get a message category to break on when a message with that category passes through the storage filter. |
| [ID3D12InfoQueue::GetBreakOnID](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getbreakonid.md) | Get a message identifier to break on when a message with that identifier passes through the storage filter. |
| [ID3D12InfoQueue::GetBreakOnSeverity](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getbreakonseverity.md) | Get a message severity level to break on when a message with that severity level passes through the storage filter. |
| [ID3D12InfoQueue::GetMessageCountLimit](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getmessagecountlimit.md) | Get the maximum number of messages that can be added to the message queue. |
| [ID3D12InfoQueue::GetMessage](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getmessage.md) | Get a message from the message queue. |
| [ID3D12InfoQueue::GetMuteDebugOutput](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getmutedebugoutput.md) | Get a boolean that determines if debug output is on or off. |
| [ID3D12InfoQueue::GetNumMessagesAllowedByStorageFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getnummessagesallowedbystoragefilter.md) | Get the number of messages that were allowed to pass through a storage filter. |
| [ID3D12InfoQueue::GetNumMessagesDeniedByStorageFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getnummessagesdeniedbystoragefilter.md) | Get the number of messages that were denied passage through a storage filter. |
| [ID3D12InfoQueue::GetNumMessagesDiscardedByMessageCountLimit](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getnummessagesdiscardedbymessagecountlimit.md) | Get the number of messages that were discarded due to the message count limit. |
| [ID3D12InfoQueue::GetNumStoredMessagesAllowedByRetrievalFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getnumstoredmessagesallowedbyretrievalfilter.md) | Get the number of messages that are able to pass through a retrieval filter. |
| [ID3D12InfoQueue::GetNumStoredMessages](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getnumstoredmessages.md) | Get the number of messages currently stored in the message queue. |
| [ID3D12InfoQueue::GetRetrievalFilterStackSize](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getretrievalfilterstacksize.md) | Get the size of the retrieval-filter stack in bytes. |
| [ID3D12InfoQueue::GetRetrievalFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getretrievalfilter.md) | Get the retrieval filter at the top of the retrieval-filter stack. |
| [ID3D12InfoQueue::GetStorageFilterStackSize](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getstoragefilterstacksize.md) | Get the size of the storage-filter stack in bytes. |
| [ID3D12InfoQueue::GetStorageFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-getstoragefilter.md) | Get the storage filter at the top of the storage-filter stack. |
| [ID3D12InfoQueue::PopRetrievalFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-popretrievalfilter.md) | Pop a retrieval filter from the top of the retrieval-filter stack. |
| [ID3D12InfoQueue::PopStorageFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-popstoragefilter.md) | Pop a storage filter from the top of the storage-filter stack. |
| [ID3D12InfoQueue::PushCopyOfRetrievalFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-pushcopyofretrievalfilter.md) | Push a copy of retrieval filter currently on the top of the retrieval-filter stack onto the retrieval-filter stack. |
| [ID3D12InfoQueue::PushCopyOfStorageFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-pushcopyofstoragefilter.md) | Push a copy of storage filter currently on the top of the storage-filter stack onto the storage-filter stack. |
| [ID3D12InfoQueue::PushEmptyRetrievalFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-pushemptyretrievalfilter.md) | Push an empty retrieval filter onto the retrieval-filter stack. |
| [ID3D12InfoQueue::PushEmptyStorageFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-pushemptystoragefilter.md) | Push an empty storage filter onto the storage-filter stack. |
| [ID3D12InfoQueue::PushRetrievalFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-pushretrievalfilter.md) | Push a retrieval filter onto the retrieval-filter stack. |
| [ID3D12InfoQueue::PushStorageFilter](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-pushstoragefilter.md) | Push a storage filter onto the storage-filter stack. |
| [ID3D12InfoQueue::SetBreakOnCategory](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-setbreakoncategory.md) | Set a message category to break on when a message with that category passes through the storage filter. |
| [ID3D12InfoQueue::SetBreakOnID](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-setbreakonid.md) | Set a message identifier to break on when a message with that identifier passes through the storage filter. |
| [ID3D12InfoQueue::SetBreakOnSeverity](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-setbreakonseverity.md) | Set a message severity level to break on when a message with that severity level passes through the storage filter. |
| [ID3D12InfoQueue::SetMessageCountLimit](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-setmessagecountlimit.md) | Set the maximum number of messages that can be added to the message queue. |
| [ID3D12InfoQueue::SetMuteDebugOutput](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12infoqueue-setmutedebugoutput.md) | Set a boolean that turns the debug output on or off. |
| [ID3D12LibraryReflection::GetDesc](..\d3d12shader\nf-d3d12shader-id3d12libraryreflection-getdesc.md) | Fills the library descriptor structure for the library reflection. |
| [ID3D12LibraryReflection::GetFunctionByIndex](..\d3d12shader\nf-d3d12shader-id3d12libraryreflection-getfunctionbyindex.md) | Gets the function reflector. |
| [ID3D12Object::GetPrivateData](..\d3d12\nf-d3d12-id3d12object-getprivatedata.md) | Gets application-defined data from a device object. |
| [ID3D12Object::SetName](..\d3d12\nf-d3d12-id3d12object-setname.md) | Associates a name with the device object. This name is for use in debug diagnostics and tools. |
| [ID3D12Object::SetPrivateDataInterface](..\d3d12\nf-d3d12-id3d12object-setprivatedatainterface.md) | Associates an IUnknown-derived interface with the device object and associates that interface with an application-defined GUID. |
| [ID3D12Object::SetPrivateData](..\d3d12\nf-d3d12-id3d12object-setprivatedata.md) | Sets application-defined data to a device object and associates that data with an application-defined GUID. |
| [ID3D12PipelineLibrary1::LoadPipeline](..\d3d12\nf-d3d12-id3d12pipelinelibrary1-loadpipeline.md) | Retrieves the requested PSO from the library. The pipeline stream description is matched against the library database and remembered in order to prevent duplication of PSO contents. |
| [ID3D12PipelineLibrary::GetSerializedSize](..\d3d12\nf-d3d12-id3d12pipelinelibrary-getserializedsize.md) | Returns the amount of memory required to serialize the current contents of the database. |
| [ID3D12PipelineLibrary::LoadComputePipeline](..\d3d12\nf-d3d12-id3d12pipelinelibrary-loadcomputepipeline.md) | Retrieves the requested PSO from the library. The input desc is matched against the data in the current library database, and remembered in order to prevent duplication of PSO contents. |
| [ID3D12PipelineLibrary::LoadGraphicsPipeline](..\d3d12\nf-d3d12-id3d12pipelinelibrary-loadgraphicspipeline.md) | Retrieves the requested PSO from the library. |
| [ID3D12PipelineLibrary::Serialize](..\d3d12\nf-d3d12-id3d12pipelinelibrary-serialize.md) | Writes the contents of the library to the provided memory, to be provided back to the runtime at a later time. |
| [ID3D12PipelineLibrary::StorePipeline](..\d3d12\nf-d3d12-id3d12pipelinelibrary-storepipeline.md) | Adds the input PSO to an internal database with the corresponding name. |
| [ID3D12PipelineState::GetCachedBlob](..\d3d12\nf-d3d12-id3d12pipelinestate-getcachedblob.md) | Gets the cached blob representing the pipeline state. |
| [ID3D12Resource::GetGPUVirtualAddress](..\d3d12\nf-d3d12-id3d12resource-getgpuvirtualaddress.md) | This method returns the GPU virtual address of a buffer resource. |
| [ID3D12Resource::GetHeapProperties](..\d3d12\nf-d3d12-id3d12resource-getheapproperties.md) | Retrieves the properties of the resource heap, for placed and committed resources. |
| [ID3D12Resource::Map](..\d3d12\nf-d3d12-id3d12resource-map.md) | Gets a CPU pointer to the specified subresource in the resource, but may not disclose the pointer value to applications. Map also invalidates the CPU cache, when necessary, so that CPU reads to this address reflect any modifications made by the GPU. |
| [ID3D12Resource::ReadFromSubresource](..\d3d12\nf-d3d12-id3d12resource-readfromsubresource.md) | Uses the CPU to copy data from a subresource, enabling the CPU to read the contents of most textures with undefined layouts. |
| [ID3D12Resource::Unmap](..\d3d12\nf-d3d12-id3d12resource-unmap.md) | Invalidates the CPU pointer to the specified subresource in the resource. Unmap also flushes the CPU cache, when necessary, so that GPU reads to this address reflect any modifications made by the CPU. |
| [ID3D12Resource::WriteToSubresource](..\d3d12\nf-d3d12-id3d12resource-writetosubresource.md) | Uses the CPU to copy data into a subresource, enabling the CPU to modify the contents of most textures with undefined layouts. |
| [ID3D12RootSignatureDeserializer::GetRootSignatureDesc](..\d3d12\nf-d3d12-id3d12rootsignaturedeserializer-getrootsignaturedesc.md) | Gets the layout of the root signature. |
| [ID3D12ShaderReflection::GetBitwiseInstructionCount](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getbitwiseinstructioncount.md) | Gets the number of bitwise instructions. |
| [ID3D12ShaderReflection::GetConstantBufferByIndex](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getconstantbufferbyindex.md) | Gets a constant buffer by index. |
| [ID3D12ShaderReflection::GetConstantBufferByName](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getconstantbufferbyname.md) | Gets a constant buffer by name. |
| [ID3D12ShaderReflection::GetConversionInstructionCount](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getconversioninstructioncount.md) | Gets the number of conversion instructions. |
| [ID3D12ShaderReflection::GetDesc](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getdesc.md) | Gets a shader description. |
| [ID3D12ShaderReflection::GetGSInputPrimitive](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getgsinputprimitive.md) | Gets the geometry-shader input-primitive description. |
| [ID3D12ShaderReflection::GetInputParameterDesc](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getinputparameterdesc.md) | Gets an input-parameter description for a shader. |
| [ID3D12ShaderReflection::GetMinFeatureLevel](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getminfeaturelevel.md) | Gets the minimum feature level. |
| [ID3D12ShaderReflection::GetMovInstructionCount](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getmovinstructioncount.md) | Gets the number of Mov instructions. |
| [ID3D12ShaderReflection::GetMovcInstructionCount](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getmovcinstructioncount.md) | Gets the number of Movc instructions. |
| [ID3D12ShaderReflection::GetNumInterfaceSlots](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getnuminterfaceslots.md) | Gets the number of interface slots in a shader. |
| [ID3D12ShaderReflection::GetOutputParameterDesc](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getoutputparameterdesc.md) | Gets an output-parameter description for a shader. |
| [ID3D12ShaderReflection::GetPatchConstantParameterDesc](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getpatchconstantparameterdesc.md) | Gets a patch-constant parameter description for a shader. |
| [ID3D12ShaderReflection::GetRequiresFlags](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getrequiresflags.md) | Gets a group of flags that indicates the requirements of a shader. |
| [ID3D12ShaderReflection::GetResourceBindingDescByName](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getresourcebindingdescbyname.md) | Gets a description of how a resource is bound to a shader. |
| [ID3D12ShaderReflection::GetResourceBindingDesc](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getresourcebindingdesc.md) | Gets a description of how a resource is bound to a shader. |
| [ID3D12ShaderReflection::GetThreadGroupSize](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getthreadgroupsize.md) | Retrieves the sizes, in units of threads, of the X, Y, and Z dimensions of the shader's thread-group grid. |
| [ID3D12ShaderReflection::GetVariableByName](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-getvariablebyname.md) | Gets a variable by name. |
| [ID3D12ShaderReflection::IsSampleFrequencyShader](..\d3d12shader\nf-d3d12shader-id3d12shaderreflection-issamplefrequencyshader.md) | Indicates whether a shader is a sample frequency shader. |
| [ID3D12ShaderReflectionConstantBuffer::GetDesc](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectionconstantbuffer-getdesc.md) | Gets a constant-buffer description. |
| [ID3D12ShaderReflectionConstantBuffer::GetVariableByIndex](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectionconstantbuffer-getvariablebyindex.md) | Gets a shader-reflection variable by index. |
| [ID3D12ShaderReflectionConstantBuffer::GetVariableByName](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectionconstantbuffer-getvariablebyname.md) | Gets a shader-reflection variable by name. |
| [ID3D12ShaderReflectionType::GetBaseClass](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectiontype-getbaseclass.md) | Gets an ID3D12ShaderReflectionType Interface interface containing the variable base class type. |
| [ID3D12ShaderReflectionType::GetDesc](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectiontype-getdesc.md) | Gets the description of a shader-reflection-variable type. |
| [ID3D12ShaderReflectionType::GetInterfaceByIndex](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectiontype-getinterfacebyindex.md) | Gets an interface by index. |
| [ID3D12ShaderReflectionType::GetMemberTypeByIndex](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectiontype-getmembertypebyindex.md) | Gets a shader-reflection-variable type by index. |
| [ID3D12ShaderReflectionType::GetMemberTypeByName](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectiontype-getmembertypebyname.md) | Gets a shader-reflection-variable type by name. |
| [ID3D12ShaderReflectionType::GetMemberTypeName](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectiontype-getmembertypename.md) | Gets a shader-reflection-variable type. |
| [ID3D12ShaderReflectionType::GetNumInterfaces](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectiontype-getnuminterfaces.md) | Gets the number of interfaces. |
| [ID3D12ShaderReflectionType::GetSubType](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectiontype-getsubtype.md) | Gets the base class of a class. |
| [ID3D12ShaderReflectionType::ImplementsInterface](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectiontype-implementsinterface.md) | Indicates whether a class type implements an interface. |
| [ID3D12ShaderReflectionType::IsEqual](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectiontype-isequal.md) | Indicates whether two ID3D12ShaderReflectionType Interface pointers have the same underlying type. |
| [ID3D12ShaderReflectionType::IsOfType](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectiontype-isoftype.md) | Indicates whether a variable is of the specified type. |
| [ID3D12ShaderReflectionVariable::GetBuffer](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectionvariable-getbuffer.md) | Returns the ID3D12ShaderReflectionConstantBuffer of the present ID3D12ShaderReflectionVariable. |
| [ID3D12ShaderReflectionVariable::GetDesc](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectionvariable-getdesc.md) | Gets a shader-variable description. |
| [ID3D12ShaderReflectionVariable::GetInterfaceSlot](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectionvariable-getinterfaceslot.md) | Gets the corresponding interface slot for a variable that represents an interface pointer. |
| [ID3D12ShaderReflectionVariable::GetType](..\d3d12shader\nf-d3d12shader-id3d12shaderreflectionvariable-gettype.md) | Gets a shader-variable type. |
| [ID3D12SharingContract::Present](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12sharingcontract-present.md) | Shares a resource (or subresource) between the D3D layers and diagnostics tools. |
| [ID3D12SharingContract::SharedFenceSignal](..\d3d12sdklayers\nf-d3d12sdklayers-id3d12sharingcontract-sharedfencesignal.md) | Signals a shared fence between the D3D layers and diagnostics tools. |
| [ID3D12Tools::EnableShaderInstrumentation](..\d3d12\nf-d3d12-id3d12tools-enableshaderinstrumentation.md) | This method enables tools such as PIX to instrument shaders. |
| [ID3D12Tools::ShaderInstrumentationEnabled](..\d3d12\nf-d3d12-id3d12tools-shaderinstrumentationenabled.md) | Determines whether shader instrumentation is enabled. |
| [ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion](..\d3d12\nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion.md) | Converts root signature description structures to a requested version. |
| [ID3D12VersionedRootSignatureDeserializer::GetUnconvertedRootSignatureDesc](..\d3d12\nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc.md) | Gets the layout of the root signature, without converting between root signature versions. |
