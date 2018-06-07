---
UID: TP:direct3ddxgi
ms.assetid: 13788405-72f0-3653-b458-78589ede8b8a
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# DXGI



Overview of the DXGI technology.

To develop DXGI, you need these headers:

 * [dxgi.h](..\dxgi\index.md)
 * [dxgi1_2.h](..\dxgi1_2\index.md)
 * [dxgi1_3.h](..\dxgi1_3\index.md)
 * [dxgi1_4.h](..\dxgi1_4\index.md)
 * [dxgi1_5.h](..\dxgi1_5\index.md)
 * [dxgi1_6.h](..\dxgi1_6\index.md)
 * [dxgicommon.h](..\dxgicommon\index.md)
 * [dxgidebug.h](..\dxgidebug\index.md)
 * [dxgiformat.h](..\dxgiformat\index.md)

For the programming guide, see [DXGI](/windows/desktop/direct3ddxgi).

## Functions

| Title   | Description   |
| ---- |:---- |
| [CreateDXGIFactory function](..\dxgi\nf-dxgi-createdxgifactory.md) | Creates a DXGI 1.0 factory that you can use to generate other DXGI objects. |
| [CreateDXGIFactory1 function](..\dxgi\nf-dxgi-createdxgifactory1.md) | Creates a DXGI 1.1 factory that you can use to generate other DXGI objects. |
| [CreateDXGIFactory2 function](..\dxgi1_3\nf-dxgi1_3-createdxgifactory2.md) | Creates a DXGI 1.3 factory that you can use to generate other DXGI objects. |
| [DXGIDeclareAdapterRemovalSupport function](..\dxgi1_6\nf-dxgi1_6-dxgideclareadapterremovalsupport.md) | Allows a process to indicate that it's resilient to any of its graphics devices being removed. |
| [DXGIGetDebugInterface function](..\dxgidebug\nf-dxgidebug-dxgigetdebuginterface.md) | Retrieves a debugging interface. |
| [DXGIGetDebugInterface1 function](..\dxgi1_3\nf-dxgi1_3-dxgigetdebuginterface1.md) | Retrieves an interface that Windows Store apps use for debugging the Microsoft DirectX Graphics Infrastructure (DXGI). |

## Structures

| Title   | Description   |
| ---- |:---- |
| [DXGI_ADAPTER_DESC structure](..\dxgi\ns-dxgi-dxgi_adapter_desc.md) | Describes an adapter (or video card) by using DXGI 1.0. |
| [DXGI_ADAPTER_DESC1 structure](..\dxgi\ns-dxgi-dxgi_adapter_desc1.md) | Describes an adapter (or video card) using DXGI 1.1. |
| [DXGI_ADAPTER_DESC2 structure](..\dxgi1_2\ns-dxgi1_2-dxgi_adapter_desc2.md) | Describes an adapter (or video card) that uses Microsoft DirectX Graphics Infrastructure (DXGI) 1.2. |
| [DXGI_ADAPTER_DESC3 structure](..\dxgi1_6\ns-dxgi1_6-dxgi_adapter_desc3.md) | Describes an adapter (or video card) that uses Microsoft DirectX Graphics Infrastructure (DXGI) 1.6. |
| [DXGI_DECODE_SWAP_CHAIN_DESC structure](..\dxgi1_3\ns-dxgi1_3-dxgi_decode_swap_chain_desc.md) | Used with IDXGIFactoryMedia |
| [DXGI_DISPLAY_COLOR_SPACE structure](..\dxgi\ns-dxgi-dxgi_display_color_space.md) | Don't use this structure; it is not supported and it will be removed from the header in a future release. |
| [DXGI_FRAME_STATISTICS structure](..\dxgi\ns-dxgi-dxgi_frame_statistics.md) | Describes timing and presentation statistics for a frame. |
| [DXGI_FRAME_STATISTICS_MEDIA structure](..\dxgi1_3\ns-dxgi1_3-dxgi_frame_statistics_media.md) | Used to verify system approval for the app's custom present duration (custom refresh rate). |
| [DXGI_HDR_METADATA_HDR10 structure](..\dxgi1_5\ns-dxgi1_5-dxgi_hdr_metadata_hdr10.md) | Describes the metadata for HDR10, used when video is compressed using High Efficiency Video Coding (HEVC). |
| [DXGI_INFO_QUEUE_FILTER structure](..\dxgidebug\ns-dxgidebug-dxgi_info_queue_filter.md) | Describes a debug message filter, which contains lists of message types to allow and deny. |
| [DXGI_INFO_QUEUE_FILTER_DESC structure](..\dxgidebug\ns-dxgidebug-dxgi_info_queue_filter_desc.md) | Describes the types of messages to allow or deny to pass through a filter. |
| [DXGI_INFO_QUEUE_MESSAGE structure](..\dxgidebug\ns-dxgidebug-dxgi_info_queue_message.md) | Describes a debug message in the information queue. |
| [DXGI_MAPPED_RECT structure](..\dxgi\ns-dxgi-dxgi_mapped_rect.md) | Describes a mapped rectangle that is used to access a surface. |
| [DXGI_MATRIX_3X2_F structure](..\dxgi1_3\ns-dxgi1_3-dxgi_matrix_3x2_f.md) | Represents a 3x2 matrix. Used with GetMatrixTransform and SetMatrixTransform to indicate the scaling and translation transform for SwapChainPanel swap chains. |
| [DXGI_MODE_DESC1 structure](..\dxgi1_2\ns-dxgi1_2-dxgi_mode_desc1.md) | Describes a display mode and whether the display mode supports stereo. |
| [DXGI_OUTDUPL_DESC structure](..\dxgi1_2\ns-dxgi1_2-dxgi_outdupl_desc.md) | The DXGI_OUTDUPL_DESC structure describes the dimension of the output and the surface that contains the desktop image. The format of the desktop image is always DXGI_FORMAT_B8G8R8A8_UNORM. |
| [DXGI_OUTDUPL_FRAME_INFO structure](..\dxgi1_2\ns-dxgi1_2-dxgi_outdupl_frame_info.md) | The DXGI_OUTDUPL_FRAME_INFO structure describes the current desktop image. |
| [DXGI_OUTDUPL_MOVE_RECT structure](..\dxgi1_2\ns-dxgi1_2-dxgi_outdupl_move_rect.md) | The DXGI_OUTDUPL_MOVE_RECT structure describes the movement of a rectangle. |
| [DXGI_OUTDUPL_POINTER_POSITION structure](..\dxgi1_2\ns-dxgi1_2-dxgi_outdupl_pointer_position.md) | The DXGI_OUTDUPL_POINTER_POSITION structure describes the position of the hardware cursor. |
| [DXGI_OUTDUPL_POINTER_SHAPE_INFO structure](..\dxgi1_2\ns-dxgi1_2-dxgi_outdupl_pointer_shape_info.md) | The DXGI_OUTDUPL_POINTER_SHAPE_INFO structure describes information about the cursor shape. |
| [DXGI_OUTPUT_DESC structure](..\dxgi\ns-dxgi-dxgi_output_desc.md) | Describes an output or physical connection between the adapter (video card) and a device. |
| [DXGI_OUTPUT_DESC1 structure](..\dxgi1_6\ns-dxgi1_6-dxgi_output_desc1.md) | Describes an output or physical connection between the adapter (video card) and a device, including additional information about color capabilities and connection type. |
| [DXGI_PRESENT_PARAMETERS structure](..\dxgi1_2\ns-dxgi1_2-dxgi_present_parameters.md) | Describes information about present that helps the operating system optimize presentation. |
| [DXGI_QUERY_VIDEO_MEMORY_INFO structure](..\dxgi1_4\ns-dxgi1_4-dxgi_query_video_memory_info.md) | Describes the current video memory budgeting parameters. |
| [DXGI_RATIONAL structure](..\dxgicommon\ns-dxgicommon-dxgi_rational.md) | Represents a rational number. |
| [DXGI_SAMPLE_DESC structure](..\dxgicommon\ns-dxgicommon-dxgi_sample_desc.md) | Describes multi-sampling parameters for a resource. |
| [DXGI_SHARED_RESOURCE structure](..\dxgi\ns-dxgi-dxgi_shared_resource.md) | Represents a handle to a shared resource. |
| [DXGI_SURFACE_DESC structure](..\dxgi\ns-dxgi-dxgi_surface_desc.md) | Describes a surface. |
| [DXGI_SWAP_CHAIN_DESC structure](..\dxgi\ns-dxgi-dxgi_swap_chain_desc.md) | Describes a swap chain. |
| [DXGI_SWAP_CHAIN_DESC1 structure](..\dxgi1_2\ns-dxgi1_2-dxgi_swap_chain_desc1.md) | Describes a swap chain. |
| [DXGI_SWAP_CHAIN_FULLSCREEN_DESC structure](..\dxgi1_2\ns-dxgi1_2-dxgi_swap_chain_fullscreen_desc.md) | Describes full-screen mode for a swap chain. |
| [_LUID structure](..\dxgi\ns-dxgi-_luid.md) | Describes a local identifier for an adapter. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [DXGI_ADAPTER_FLAG enumeration](..\dxgi\ne-dxgi-dxgi_adapter_flag.md) | Identifies the type of DXGI adapter. |
| [DXGI_ADAPTER_FLAG3 enumeration](..\dxgi1_6\ne-dxgi1_6-dxgi_adapter_flag3.md) | Identifies the type of DXGI adapter. |
| [DXGI_ALPHA_MODE enumeration](..\dxgi1_2\ne-dxgi1_2-dxgi_alpha_mode.md) | Identifies the alpha value, transparency behavior, of a surface. |
| [DXGI_COLOR_SPACE_TYPE enumeration](..\dxgicommon\ne-dxgicommon-dxgi_color_space_type.md) | Specifies color space types. |
| [DXGI_COMPUTE_PREEMPTION_GRANULARITY enumeration](..\dxgi1_2\ne-dxgi1_2-dxgi_compute_preemption_granularity.md) | Identifies the granularity at which the graphics processing unit (GPU) can be preempted from performing its current compute task. |
| [DXGI_DEBUG_RLO_FLAGS enumeration](..\dxgidebug\ne-dxgidebug-dxgi_debug_rlo_flags.md) | Flags used with ReportLiveObjects to specify the amount of info to report about an object's lifetime. |
| [DXGI_FEATURE enumeration](..\dxgi1_5\ne-dxgi1_5-dxgi_feature.md) | Specifies a range of hardware features, to be used when checking for feature support. |
| [DXGI_FORMAT enumeration](..\dxgiformat\ne-dxgiformat-dxgi_format.md) | Resource data formats, including fully-typed and typeless formats. A list of modifiers at the bottom of the page more fully describes each format type. |
| [DXGI_FRAME_PRESENTATION_MODE enumeration](..\dxgi1_3\ne-dxgi1_3-dxgi_frame_presentation_mode.md) | Indicates options for presenting frames to the swap chain. |
| [DXGI_GPU_PREFERENCE enumeration](..\dxgi1_6\ne-dxgi1_6-dxgi_gpu_preference.md) | The preference of GPU for the app to run on. |
| [DXGI_GRAPHICS_PREEMPTION_GRANULARITY enumeration](..\dxgi1_2\ne-dxgi1_2-dxgi_graphics_preemption_granularity.md) | Identifies the granularity at which the graphics processing unit (GPU) can be preempted from performing its current graphics rendering task. |
| [DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS enumeration](..\dxgi1_6\ne-dxgi1_6-dxgi_hardware_composition_support_flags.md) | Describes which levels of hardware composition are supported. |
| [DXGI_HDR_METADATA_TYPE enumeration](..\dxgi1_5\ne-dxgi1_5-dxgi_hdr_metadata_type.md) | Specifies the header metadata type. |
| [DXGI_INFO_QUEUE_MESSAGE_CATEGORY enumeration](..\dxgidebug\ne-dxgidebug-dxgi_info_queue_message_category.md) | Values that specify categories of debug messages. |
| [DXGI_INFO_QUEUE_MESSAGE_SEVERITY enumeration](..\dxgidebug\ne-dxgidebug-dxgi_info_queue_message_severity.md) | Values that specify debug message severity levels for an information queue. |
| [DXGI_MEMORY_SEGMENT_GROUP enumeration](..\dxgi1_4\ne-dxgi1_4-dxgi_memory_segment_group.md) | Specifies the memory segment group to use. |
| [DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS enumeration](..\dxgi1_3\ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags.md) | Options for swap-chain color space. |
| [DXGI_OUTDUPL_POINTER_SHAPE_TYPE enumeration](..\dxgi1_2\ne-dxgi1_2-dxgi_outdupl_pointer_shape_type.md) | Identifies the type of pointer shape. |
| [DXGI_OVERLAY_COLOR_SPACE_SUPPORT_FLAG enumeration](..\dxgi1_4\ne-dxgi1_4-dxgi_overlay_color_space_support_flag.md) | Specifies support for overlay color space. |
| [DXGI_OVERLAY_SUPPORT_FLAG enumeration](..\dxgi1_3\ne-dxgi1_3-dxgi_overlay_support_flag.md) | Specifies overlay support to check for in a call to IDXGIOutput3 |
| [DXGI_RESIDENCY enumeration](..\dxgi\ne-dxgi-dxgi_residency.md) | Flags indicating the memory location of a resource. |
| [DXGI_SCALING enumeration](..\dxgi1_2\ne-dxgi1_2-dxgi_scaling.md) | Identifies resize behavior when the back-buffer size does not match the size of the target output. |
| [DXGI_SWAP_CHAIN_COLOR_SPACE_SUPPORT_FLAG enumeration](..\dxgi1_4\ne-dxgi1_4-dxgi_swap_chain_color_space_support_flag.md) | Specifies color space support for the swap chain. |
| [DXGI_SWAP_CHAIN_FLAG enumeration](..\dxgi\ne-dxgi-dxgi_swap_chain_flag.md) | Options for swap-chain behavior. |
| [DXGI_SWAP_EFFECT enumeration](..\dxgi\ne-dxgi-dxgi_swap_effect.md) | Options for handling pixels in a display surface after calling IDXGISwapChain1 |
| [_DXGI_OFFER_RESOURCE_FLAGS enumeration](..\dxgi1_5\ne-dxgi1_5-_dxgi_offer_resource_flags.md) | Specifies flags for the OfferResources1 method. |
| [_DXGI_OFFER_RESOURCE_PRIORITY enumeration](..\dxgi1_2\ne-dxgi1_2-_dxgi_offer_resource_priority.md) | Identifies the importance of a resource’s content when you call the IDXGIDevice2 |
| [_DXGI_RECLAIM_RESOURCE_RESULTS enumeration](..\dxgi1_5\ne-dxgi1_5-_dxgi_reclaim_resource_results.md) | Specifies result flags for the ReclaimResources1 method. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IDXGIAdapter interface](..\dxgi\nn-dxgi-idxgiadapter.md) | The IDXGIAdapter interface represents a display subsystem (including one or more GPUs, DACs and video memory). |
| [IDXGIAdapter1 interface](..\dxgi\nn-dxgi-idxgiadapter1.md) | The IDXGIAdapter1 interface represents a display sub-system (including one or more GPU's, DACs and video memory). |
| [IDXGIAdapter2 interface](..\dxgi1_2\nn-dxgi1_2-idxgiadapter2.md) | The IDXGIAdapter2 interface represents a display subsystem, which includes one or more GPUs, DACs, and video memory. |
| [IDXGIAdapter3 interface](..\dxgi1_4\nn-dxgi1_4-idxgiadapter3.md) | This interface adds some memory residency methods, for budgeting and reserving physical memory. |
| [IDXGIAdapter4 interface](..\dxgi1_6\nn-dxgi1_6-idxgiadapter4.md) | This interface represents a display subsystem, and extends this family of interfaces to expose a method to check for an adapter's compatibility with Arbitrary Code Guard (ACG). |
| [IDXGIDebug interface](..\dxgidebug\nn-dxgidebug-idxgidebug.md) | This interface controls debug settings, and can only be used if the debug layer is turned on. |
| [IDXGIDebug1 interface](..\dxgidebug\nn-dxgidebug-idxgidebug1.md) | Controls debug settings for Microsoft DirectX Graphics Infrastructure (DXGI). You can use the IDXGIDebug1 interface in Windows Store apps. |
| [IDXGIDecodeSwapChain interface](..\dxgi1_3\nn-dxgi1_3-idxgidecodeswapchain.md) | Represents a swap chain that is used by desktop media apps to decode video data and show it on a DirectComposition surface. |
| [IDXGIDevice interface](..\dxgi\nn-dxgi-idxgidevice.md) | An IDXGIDevice interface implements a derived class for DXGI objects that produce image data. |
| [IDXGIDevice1 interface](..\dxgi\nn-dxgi-idxgidevice1.md) | An IDXGIDevice1 interface implements a derived class for DXGI objects that produce image data. |
| [IDXGIDevice2 interface](..\dxgi1_2\nn-dxgi1_2-idxgidevice2.md) | The IDXGIDevice2 interface implements a derived class for DXGI objects that produce image data. The interface exposes methods to block CPU processing until the GPU completes processing, and to offer resources to the operating system. |
| [IDXGIDevice3 interface](..\dxgi1_3\nn-dxgi1_3-idxgidevice3.md) | The IDXGIDevice3 interface implements a derived class for DXGI objects that produce image data. The interface exposes a method to trim graphics memory usage by the DXGI device. |
| [IDXGIDevice4 interface](..\dxgi1_5\nn-dxgi1_5-idxgidevice4.md) | This interface provides updated methods to offer and reclaim resources. |
| [IDXGIDeviceSubObject interface](..\dxgi\nn-dxgi-idxgidevicesubobject.md) | Inherited from objects that are tied to the device so that they can retrieve a pointer to it. |
| [IDXGIDisplayControl interface](..\dxgi1_2\nn-dxgi1_2-idxgidisplaycontrol.md) | The IDXGIDisplayControl interface exposes methods to indicate user preference for the operating system's stereoscopic 3D display behavior and to set stereoscopic 3D display status to enable or disable. |
| [IDXGIFactory interface](..\dxgi\nn-dxgi-idxgifactory.md) | An IDXGIFactory interface implements methods for generating DXGI objects (which handle full screen transitions). |
| [IDXGIFactory1 interface](..\dxgi\nn-dxgi-idxgifactory1.md) | The IDXGIFactory1 interface implements methods for generating DXGI objects. |
| [IDXGIFactory2 interface](..\dxgi1_2\nn-dxgi1_2-idxgifactory2.md) | The IDXGIFactory2 interface includes methods to create a newer version swap chain with more features than IDXGISwapChain and to monitor stereoscopic 3D capabilities. |
| [IDXGIFactory3 interface](..\dxgi1_3\nn-dxgi1_3-idxgifactory3.md) | Enables creating Microsoft DirectX Graphics Infrastructure (DXGI) objects. |
| [IDXGIFactory4 interface](..\dxgi1_4\nn-dxgi1_4-idxgifactory4.md) | Enables creating Microsoft DirectX Graphics Infrastructure (DXGI) objects. |
| [IDXGIFactory5 interface](..\dxgi1_5\nn-dxgi1_5-idxgifactory5.md) | This interface enables a single method to support variable refresh rate displays. |
| [IDXGIFactory6 interface](..\dxgi1_6\nn-dxgi1_6-idxgifactory6.md) | This interface enables a single method that enumerates graphics adapters based on a given GPU preference. |
| [IDXGIFactoryMedia interface](..\dxgi1_3\nn-dxgi1_3-idxgifactorymedia.md) | Creates swap chains for desktop media apps that use DirectComposition surfaces to decode and display video. |
| [IDXGIInfoQueue interface](..\dxgidebug\nn-dxgidebug-idxgiinfoqueue.md) | This interface controls the debug information queue, and can only be used if the debug layer is turned on. |
| [IDXGIKeyedMutex interface](..\dxgi\nn-dxgi-idxgikeyedmutex.md) | Represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices. |
| [IDXGIObject interface](..\dxgi\nn-dxgi-idxgiobject.md) | An IDXGIObject interface is a base interface for all DXGI objects; IDXGIObject supports associating caller-defined (private data) with an object and retrieval of an interface to the parent object. |
| [IDXGIOutput interface](..\dxgi\nn-dxgi-idxgioutput.md) | An IDXGIOutput interface represents an adapter output (such as a monitor). |
| [IDXGIOutput1 interface](..\dxgi1_2\nn-dxgi1_2-idxgioutput1.md) | An IDXGIOutput1 interface represents an adapter output (such as a monitor). |
| [IDXGIOutput2 interface](..\dxgi1_3\nn-dxgi1_3-idxgioutput2.md) | Represents an adapter output (such as a monitor). The IDXGIOutput2 interface exposes a method to check for multiplane overlay support on the primary output adapter. |
| [IDXGIOutput3 interface](..\dxgi1_3\nn-dxgi1_3-idxgioutput3.md) | Represents an adapter output (such as a monitor). The IDXGIOutput3 interface exposes a method to check for overlay support. |
| [IDXGIOutput4 interface](..\dxgi1_4\nn-dxgi1_4-idxgioutput4.md) | Represents an adapter output (such as a monitor). The IDXGIOutput4 interface exposes a method to check for overlay color space support. |
| [IDXGIOutput5 interface](..\dxgi1_5\nn-dxgi1_5-idxgioutput5.md) | Represents an adapter output (such as a monitor). The IDXGIOutput5 interface exposes a single method to specify a list of supported formats for fullscreen surfaces. |
| [IDXGIOutput6 interface](..\dxgi1_6\nn-dxgi1_6-idxgioutput6.md) | Represents an adapter output (such as a monitor). The IDXGIOutput6 interface exposes methods to provide specific monitor capabilities. |
| [IDXGIOutputDuplication interface](..\dxgi1_2\nn-dxgi1_2-idxgioutputduplication.md) | The IDXGIOutputDuplication interface accesses and manipulates the duplicated desktop image. |
| [IDXGIResource interface](..\dxgi\nn-dxgi-idxgiresource.md) | An IDXGIResource interface allows resource sharing and identifies the memory that a resource resides in. |
| [IDXGIResource1 interface](..\dxgi1_2\nn-dxgi1_2-idxgiresource1.md) | An IDXGIResource1 interface extends the IDXGIResource interface by adding support for creating a subresource surface object and for creating a handle to a shared resource. |
| [IDXGISurface interface](..\dxgi\nn-dxgi-idxgisurface.md) | The IDXGISurface interface implements methods for image-data objects. |
| [IDXGISurface1 interface](..\dxgi\nn-dxgi-idxgisurface1.md) | The IDXGISurface1 interface extends the IDXGISurface by adding support for using Windows Graphics Device Interface (GDI) to render to a Microsoft DirectX Graphics Infrastructure (DXGI) surface. |
| [IDXGISurface2 interface](..\dxgi1_2\nn-dxgi1_2-idxgisurface2.md) | The IDXGISurface2 interface extends the IDXGISurface1 interface by adding support for subresource surfaces and getting a handle to a shared resource. |
| [IDXGISwapChain interface](..\dxgi\nn-dxgi-idxgiswapchain.md) | An IDXGISwapChain interface implements one or more surfaces for storing rendered data before presenting it to an output. |
| [IDXGISwapChain1 interface](..\dxgi1_2\nn-dxgi1_2-idxgiswapchain1.md) | Provides presentation capabilities that are enhanced from IDXGISwapChain. These presentation capabilities consist of specifying dirty rectangles and scroll rectangle to optimize the presentation. |
| [IDXGISwapChain2 interface](..\dxgi1_3\nn-dxgi1_3-idxgiswapchain2.md) | Extends IDXGISwapChain1 with methods to support swap back buffer scaling and lower-latency swap chains. |
| [IDXGISwapChain3 interface](..\dxgi1_4\nn-dxgi1_4-idxgiswapchain3.md) | Extends IDXGISwapChain2 with methods to support getting the index of the swap chain's current back buffer and support for color space. |
| [IDXGISwapChain4 interface](..\dxgi1_5\nn-dxgi1_5-idxgiswapchain4.md) | This interface exposes a single method for setting video metadata. |
| [IDXGISwapChainMedia interface](..\dxgi1_3\nn-dxgi1_3-idxgiswapchainmedia.md) | This swap chain interface allows desktop media applications to request a seamless change to a specific refresh rate. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IDXGIAdapter1::GetDesc1](..\dxgi\nf-dxgi-idxgiadapter1-getdesc1.md) | Gets a DXGI 1.1 description of an adapter (or video card). |
| [IDXGIAdapter2::GetDesc2](..\dxgi1_2\nf-dxgi1_2-idxgiadapter2-getdesc2.md) | Gets a Microsoft DirectX Graphics Infrastructure (DXGI) 1.2 description of an adapter or video card. |
| [IDXGIAdapter3::QueryVideoMemoryInfo](..\dxgi1_4\nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo.md) | This method informs the process of the current budget and process usage. |
| [IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent](..\dxgi1_4\nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent.md) | Registers to receive notification of hardware content protection teardown events. |
| [IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent](..\dxgi1_4\nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent.md) | This method establishes a correlation between a CPU synchronization object and the budget change event. |
| [IDXGIAdapter3::SetVideoMemoryReservation](..\dxgi1_4\nf-dxgi1_4-idxgiadapter3-setvideomemoryreservation.md) | This method sends the minimum required physical memory for an application, to the OS. |
| [IDXGIAdapter3::UnregisterHardwareContentProtectionTeardownStatus](..\dxgi1_4\nf-dxgi1_4-idxgiadapter3-unregisterhardwarecontentprotectionteardownstatus.md) | Unregisters an event to stop it from receiving notification of hardware content protection teardown events. |
| [IDXGIAdapter3::UnregisterVideoMemoryBudgetChangeNotification](..\dxgi1_4\nf-dxgi1_4-idxgiadapter3-unregistervideomemorybudgetchangenotification.md) | This method stops notifying a CPU synchronization object whenever a budget change occurs. An application may switch back to polling the information regularly. |
| [IDXGIAdapter4::GetDesc3](..\dxgi1_6\nf-dxgi1_6-idxgiadapter4-getdesc3.md) | Gets a Microsoft DirectX Graphics Infrastructure (DXGI) 1.6 description of an adapter or video card. This description includes information about ACG compatibility. |
| [IDXGIAdapter::CheckInterfaceSupport](..\dxgi\nf-dxgi-idxgiadapter-checkinterfacesupport.md) | Checks whether the system supports a device interface for a graphics component. |
| [IDXGIAdapter::EnumOutputs](..\dxgi\nf-dxgi-idxgiadapter-enumoutputs.md) | Enumerate adapter (video card) outputs. |
| [IDXGIAdapter::GetDesc](..\dxgi\nf-dxgi-idxgiadapter-getdesc.md) | Gets a DXGI 1.0 description of an adapter (or video card). |
| [IDXGIDebug1::DisableLeakTrackingForThread](..\dxgidebug\nf-dxgidebug-idxgidebug1-disableleaktrackingforthread.md) | Stops tracking leaks for the current thread. |
| [IDXGIDebug1::EnableLeakTrackingForThread](..\dxgidebug\nf-dxgidebug-idxgidebug1-enableleaktrackingforthread.md) | Starts tracking leaks for the current thread. |
| [IDXGIDebug1::IsLeakTrackingEnabledForThread](..\dxgidebug\nf-dxgidebug-idxgidebug1-isleaktrackingenabledforthread.md) | Gets a value indicating whether leak tracking is turned on for the current thread. |
| [IDXGIDebug::ReportLiveObjects](..\dxgidebug\nf-dxgidebug-idxgidebug-reportliveobjects.md) | Reports info about the lifetime of an object or objects. |
| [IDXGIDecodeSwapChain::GetColorSpace](..\dxgi1_3\nf-dxgi1_3-idxgidecodeswapchain-getcolorspace.md) | Gets the color space used by the swap chain. |
| [IDXGIDecodeSwapChain::GetDestSize](..\dxgi1_3\nf-dxgi1_3-idxgidecodeswapchain-getdestsize.md) | Gets the size of the destination surface to use for the video processing blit operation. |
| [IDXGIDecodeSwapChain::GetSourceRect](..\dxgi1_3\nf-dxgi1_3-idxgidecodeswapchain-getsourcerect.md) | Gets the source region that is used for the swap chain. |
| [IDXGIDecodeSwapChain::GetTargetRect](..\dxgi1_3\nf-dxgi1_3-idxgidecodeswapchain-gettargetrect.md) | Gets the rectangle that defines the target region for the video processing blit operation. |
| [IDXGIDecodeSwapChain::PresentBuffer](..\dxgi1_3\nf-dxgi1_3-idxgidecodeswapchain-presentbuffer.md) | Presents a frame on the output adapter. |
| [IDXGIDecodeSwapChain::SetColorSpace](..\dxgi1_3\nf-dxgi1_3-idxgidecodeswapchain-setcolorspace.md) | Sets the color space used by the swap chain. |
| [IDXGIDecodeSwapChain::SetDestSize](..\dxgi1_3\nf-dxgi1_3-idxgidecodeswapchain-setdestsize.md) | Sets the size of the destination surface to use for the video processing blit operation. |
| [IDXGIDecodeSwapChain::SetSourceRect](..\dxgi1_3\nf-dxgi1_3-idxgidecodeswapchain-setsourcerect.md) | Sets the rectangle that defines the source region for the video processing blit operation. |
| [IDXGIDecodeSwapChain::SetTargetRect](..\dxgi1_3\nf-dxgi1_3-idxgidecodeswapchain-settargetrect.md) | Sets the rectangle that defines the target region for the video processing blit operation. |
| [IDXGIDevice1::GetMaximumFrameLatency](..\dxgi\nf-dxgi-idxgidevice1-getmaximumframelatency.md) | Gets the number of frames that the system is allowed to queue for rendering. |
| [IDXGIDevice1::SetMaximumFrameLatency](..\dxgi\nf-dxgi-idxgidevice1-setmaximumframelatency.md) | Sets the number of frames that the system is allowed to queue for rendering. |
| [IDXGIDevice2::EnqueueSetEvent](..\dxgi1_2\nf-dxgi1_2-idxgidevice2-enqueuesetevent.md) | Flushes any outstanding rendering commands and sets the specified event object to the signaled state after all previously submitted rendering commands complete. |
| [IDXGIDevice2::OfferResources](..\dxgi1_2\nf-dxgi1_2-idxgidevice2-offerresources.md) | Allows the operating system to free the video memory of resources by discarding their content. |
| [IDXGIDevice2::ReclaimResources](..\dxgi1_2\nf-dxgi1_2-idxgidevice2-reclaimresources.md) | Restores access to resources that were previously offered by calling IDXGIDevice2 |
| [IDXGIDevice3::Trim](..\dxgi1_3\nf-dxgi1_3-idxgidevice3-trim.md) | Trims the graphics memory allocated by the IDXGIDevice3 DXGI device on the app's behalf. |
| [IDXGIDevice4::OfferResources1](..\dxgi1_5\nf-dxgi1_5-idxgidevice4-offerresources1.md) | Allows the operating system to free the video memory of resources, including both discarding the content and de-committing the memory. |
| [IDXGIDevice4::ReclaimResources1](..\dxgi1_5\nf-dxgi1_5-idxgidevice4-reclaimresources1.md) | Restores access to resources that were previously offered by calling IDXGIDevice4 |
| [IDXGIDevice::CreateSurface](..\dxgi\nf-dxgi-idxgidevice-createsurface.md) | Returns a surface. This method is used internally and you should not call it directly in your application. |
| [IDXGIDevice::GetAdapter](..\dxgi\nf-dxgi-idxgidevice-getadapter.md) | Returns the adapter for the specified device. |
| [IDXGIDevice::GetGPUThreadPriority](..\dxgi\nf-dxgi-idxgidevice-getgputhreadpriority.md) | Gets the GPU thread priority. |
| [IDXGIDevice::QueryResourceResidency](..\dxgi\nf-dxgi-idxgidevice-queryresourceresidency.md) | Gets the residency status of an array of resources. |
| [IDXGIDevice::SetGPUThreadPriority](..\dxgi\nf-dxgi-idxgidevice-setgputhreadpriority.md) | Sets the GPU thread priority. |
| [IDXGIDeviceSubObject::GetDevice](..\dxgi\nf-dxgi-idxgidevicesubobject-getdevice.md) | Retrieves the device. |
| [IDXGIDisplayControl::IsStereoEnabled](..\dxgi1_2\nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled.md) | Retrieves a Boolean value that indicates whether the operating system's stereoscopic 3D display behavior is enabled. |
| [IDXGIDisplayControl::SetStereoEnabled](..\dxgi1_2\nf-dxgi1_2-idxgidisplaycontrol-setstereoenabled.md) | Set a Boolean value to either enable or disable the operating system's stereoscopic 3D display behavior. |
| [IDXGIFactory1::EnumAdapters1](..\dxgi\nf-dxgi-idxgifactory1-enumadapters1.md) | Enumerates both adapters (video cards) with or without outputs. |
| [IDXGIFactory1::IsCurrent](..\dxgi\nf-dxgi-idxgifactory1-iscurrent.md) | Informs an application of the possible need to re-enumerate adapters. |
| [IDXGIFactory2::CreateSwapChainForComposition](..\dxgi1_2\nf-dxgi1_2-idxgifactory2-createswapchainforcomposition.md) | Creates a swap chain that you can use to send Direct3D content into the DirectComposition API or the Windows.UI.Xaml framework to compose in a window. |
| [IDXGIFactory2::CreateSwapChainForCoreWindow](..\dxgi1_2\nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow.md) | Creates a swap chain that is associated with the CoreWindow object for the output window for the swap chain. |
| [IDXGIFactory2::CreateSwapChainForHwnd](..\dxgi1_2\nf-dxgi1_2-idxgifactory2-createswapchainforhwnd.md) | Creates a swap chain that is associated with an HWND handle to the output window for the swap chain. |
| [IDXGIFactory2::GetSharedResourceAdapterLuid](..\dxgi1_2\nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid.md) | Identifies the adapter on which a shared resource object was created. |
| [IDXGIFactory2::IsWindowedStereoEnabled](..\dxgi1_2\nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled.md) | Determines whether to use stereo mode. |
| [IDXGIFactory2::RegisterOcclusionStatusEvent](..\dxgi1_2\nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent.md) | Registers to receive notification of changes in occlusion status by using event signaling. |
| [IDXGIFactory2::RegisterOcclusionStatusWindow](..\dxgi1_2\nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow.md) | Registers an application window to receive notification messages of changes of occlusion status. |
| [IDXGIFactory2::RegisterStereoStatusEvent](..\dxgi1_2\nf-dxgi1_2-idxgifactory2-registerstereostatusevent.md) | Registers to receive notification of changes in stereo status by using event signaling. |
| [IDXGIFactory2::RegisterStereoStatusWindow](..\dxgi1_2\nf-dxgi1_2-idxgifactory2-registerstereostatuswindow.md) | Registers an application window to receive notification messages of changes of stereo status. |
| [IDXGIFactory2::UnregisterOcclusionStatus](..\dxgi1_2\nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus.md) | Unregisters a window or an event to stop it from receiving notification when occlusion status changes. |
| [IDXGIFactory2::UnregisterStereoStatus](..\dxgi1_2\nf-dxgi1_2-idxgifactory2-unregisterstereostatus.md) | Unregisters a window or an event to stop it from receiving notification when stereo status changes. |
| [IDXGIFactory4::EnumAdapterByLuid](..\dxgi1_4\nf-dxgi1_4-idxgifactory4-enumadapterbyluid.md) | Outputs the IDXGIAdapter for the specified LUID. |
| [IDXGIFactory4::EnumWarpAdapter](..\dxgi1_4\nf-dxgi1_4-idxgifactory4-enumwarpadapter.md) | Provides an adapter which can be provided to D3D12CreateDevice to use the WARP renderer. |
| [IDXGIFactory5::CheckFeatureSupport](..\dxgi1_5\nf-dxgi1_5-idxgifactory5-checkfeaturesupport.md) | Used to check for hardware feature support. |
| [IDXGIFactory6::EnumAdapterByGpuPreference](..\dxgi1_6\nf-dxgi1_6-idxgifactory6-enumadapterbygpupreference.md) | Enumerates graphics adapters based on a given GPU preference. |
| [IDXGIFactory::CreateSoftwareAdapter](..\dxgi\nf-dxgi-idxgifactory-createsoftwareadapter.md) | Create an adapter interface that represents a software adapter. |
| [IDXGIFactory::CreateSwapChain](..\dxgi\nf-dxgi-idxgifactory-createswapchain.md) | Creates a swap chain. |
| [IDXGIFactory::EnumAdapters](..\dxgi\nf-dxgi-idxgifactory-enumadapters.md) | Enumerates the adapters (video cards). |
| [IDXGIFactory::GetWindowAssociation](..\dxgi\nf-dxgi-idxgifactory-getwindowassociation.md) | Get the window through which the user controls the transition to and from full screen. |
| [IDXGIFactory::MakeWindowAssociation](..\dxgi\nf-dxgi-idxgifactory-makewindowassociation.md) | Allows DXGI to monitor an application's message queue for the alt-enter key sequence (which causes the application to switch from windowed to full screen or vice versa). |
| [IDXGIFactoryMedia::CreateDecodeSwapChainForCompositionSurfaceHandle](..\dxgi1_3\nf-dxgi1_3-idxgifactorymedia-createdecodeswapchainforcompositionsurfacehandle.md) | Creates a YUV swap chain for an existing DirectComposition surface handle. |
| [IDXGIFactoryMedia::CreateSwapChainForCompositionSurfaceHandle](..\dxgi1_3\nf-dxgi1_3-idxgifactorymedia-createswapchainforcompositionsurfacehandle.md) | Creates a YUV swap chain for an existing DirectComposition surface handle. |
| [IDXGIInfoQueue::AddApplicationMessage](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-addapplicationmessage.md) | Adds a user-defined message to the message queue and sends that message to the debug output. |
| [IDXGIInfoQueue::AddMessage](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-addmessage.md) | Adds a debug message to the message queue and sends that message to the debug output. |
| [IDXGIInfoQueue::AddRetrievalFilterEntries](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-addretrievalfilterentries.md) | Adds retrieval filters to the top of the retrieval-filter stack. |
| [IDXGIInfoQueue::AddStorageFilterEntries](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-addstoragefilterentries.md) | Adds storage filters to the top of the storage-filter stack. |
| [IDXGIInfoQueue::ClearRetrievalFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-clearretrievalfilter.md) | Removes a retrieval filter from the top of the retrieval-filter stack. |
| [IDXGIInfoQueue::ClearStorageFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-clearstoragefilter.md) | Removes a storage filter from the top of the storage-filter stack. |
| [IDXGIInfoQueue::ClearStoredMessages](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-clearstoredmessages.md) | Clears all messages from the message queue. |
| [IDXGIInfoQueue::GetBreakOnCategory](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getbreakoncategory.md) | Determines whether the break on a message category is turned on or off. |
| [IDXGIInfoQueue::GetBreakOnID](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getbreakonid.md) | Determines whether the break on a message identifier is turned on or off. |
| [IDXGIInfoQueue::GetBreakOnSeverity](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getbreakonseverity.md) | Determines whether the break on a message severity level is turned on or off. |
| [IDXGIInfoQueue::GetMessageCountLimit](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getmessagecountlimit.md) | Gets the maximum number of messages that can be added to the message queue. |
| [IDXGIInfoQueue::GetMessage](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getmessage.md) | Gets a message from the message queue. |
| [IDXGIInfoQueue::GetMuteDebugOutput](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getmutedebugoutput.md) | Determines whether the debug output is turned on or off. |
| [IDXGIInfoQueue::GetNumMessagesAllowedByStorageFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getnummessagesallowedbystoragefilter.md) | Gets the number of messages that a storage filter allowed to pass through. |
| [IDXGIInfoQueue::GetNumMessagesDeniedByStorageFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getnummessagesdeniedbystoragefilter.md) | Gets the number of messages that were denied passage through a storage filter. |
| [IDXGIInfoQueue::GetNumMessagesDiscardedByMessageCountLimit](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getnummessagesdiscardedbymessagecountlimit.md) | Gets the number of messages that were discarded due to the message count limit. |
| [IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getnumstoredmessagesallowedbyretrievalfilters.md) | Gets the number of messages that can pass through a retrieval filter. |
| [IDXGIInfoQueue::GetNumStoredMessages](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getnumstoredmessages.md) | Gets the number of messages currently stored in the message queue. |
| [IDXGIInfoQueue::GetRetrievalFilterStackSize](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getretrievalfilterstacksize.md) | Gets the size of the retrieval-filter stack in bytes. |
| [IDXGIInfoQueue::GetRetrievalFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getretrievalfilter.md) | Gets the retrieval filter at the top of the retrieval-filter stack. |
| [IDXGIInfoQueue::GetStorageFilterStackSize](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getstoragefilterstacksize.md) | Gets the size of the storage-filter stack in bytes. |
| [IDXGIInfoQueue::GetStorageFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-getstoragefilter.md) | Gets the storage filter at the top of the storage-filter stack. |
| [IDXGIInfoQueue::PopRetrievalFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-popretrievalfilter.md) | Pops a retrieval filter from the top of the retrieval-filter stack. |
| [IDXGIInfoQueue::PopStorageFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-popstoragefilter.md) | Pops a storage filter from the top of the storage-filter stack. |
| [IDXGIInfoQueue::PushCopyOfRetrievalFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-pushcopyofretrievalfilter.md) | Pushes a copy of the retrieval filter that is currently on the top of the retrieval-filter stack onto the retrieval-filter stack. |
| [IDXGIInfoQueue::PushCopyOfStorageFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-pushcopyofstoragefilter.md) | Pushes a copy of the storage filter that is currently on the top of the storage-filter stack onto the storage-filter stack. |
| [IDXGIInfoQueue::PushDenyAllRetrievalFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-pushdenyallretrievalfilter.md) | Pushes a deny-all retrieval filter onto the retrieval-filter stack. |
| [IDXGIInfoQueue::PushDenyAllStorageFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-pushdenyallstoragefilter.md) | Pushes a deny-all storage filter onto the storage-filter stack. |
| [IDXGIInfoQueue::PushEmptyRetrievalFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-pushemptyretrievalfilter.md) | Pushes an empty retrieval filter onto the retrieval-filter stack. |
| [IDXGIInfoQueue::PushEmptyStorageFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-pushemptystoragefilter.md) | Pushes an empty storage filter onto the storage-filter stack. |
| [IDXGIInfoQueue::PushRetrievalFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-pushretrievalfilter.md) | Pushes a retrieval filter onto the retrieval-filter stack. |
| [IDXGIInfoQueue::PushStorageFilter](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-pushstoragefilter.md) | Pushes a storage filter onto the storage-filter stack. |
| [IDXGIInfoQueue::SetBreakOnCategory](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-setbreakoncategory.md) | Sets a message category to break on when a message with that category passes through the storage filter. |
| [IDXGIInfoQueue::SetBreakOnID](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-setbreakonid.md) | Sets a message identifier to break on when a message with that identifier passes through the storage filter. |
| [IDXGIInfoQueue::SetBreakOnSeverity](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-setbreakonseverity.md) | Sets a message severity level to break on when a message with that severity level passes through the storage filter. |
| [IDXGIInfoQueue::SetMessageCountLimit](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-setmessagecountlimit.md) | Sets the maximum number of messages that can be added to the message queue. |
| [IDXGIInfoQueue::SetMuteDebugOutput](..\dxgidebug\nf-dxgidebug-idxgiinfoqueue-setmutedebugoutput.md) | Turns the debug output on or off. |
| [IDXGIKeyedMutex::AcquireSync](..\dxgi\nf-dxgi-idxgikeyedmutex-acquiresync.md) | Using a key, acquires exclusive rendering access to a shared resource. |
| [IDXGIKeyedMutex::ReleaseSync](..\dxgi\nf-dxgi-idxgikeyedmutex-releasesync.md) | Using a key, releases exclusive rendering access to a shared resource. |
| [IDXGIObject::GetParent](..\dxgi\nf-dxgi-idxgiobject-getparent.md) | Gets the parent of the object. |
| [IDXGIObject::GetPrivateData](..\dxgi\nf-dxgi-idxgiobject-getprivatedata.md) | Get a pointer to the object's data. |
| [IDXGIObject::SetPrivateDataInterface](..\dxgi\nf-dxgi-idxgiobject-setprivatedatainterface.md) | Set an interface in the object's private data. |
| [IDXGIObject::SetPrivateData](..\dxgi\nf-dxgi-idxgiobject-setprivatedata.md) | Sets application-defined data to the object and associates that data with a GUID. |
| [IDXGIOutput1::DuplicateOutput](..\dxgi1_2\nf-dxgi1_2-idxgioutput1-duplicateoutput.md) | Creates a desktop duplication interface from the IDXGIOutput1 interface that represents an adapter output. |
| [IDXGIOutput1::FindClosestMatchingMode1](..\dxgi1_2\nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1.md) | Finds the display mode that most closely matches the requested display mode. |
| [IDXGIOutput1::GetDisplayModeList1](..\dxgi1_2\nf-dxgi1_2-idxgioutput1-getdisplaymodelist1.md) | Gets the display modes that match the requested format and other input options. |
| [IDXGIOutput1::GetDisplaySurfaceData1](..\dxgi1_2\nf-dxgi1_2-idxgioutput1-getdisplaysurfacedata1.md) | Copies the display surface (front buffer) to a user-provided resource. |
| [IDXGIOutput2::SupportsOverlays](..\dxgi1_3\nf-dxgi1_3-idxgioutput2-supportsoverlays.md) | Queries an adapter output for multiplane overlay support. |
| [IDXGIOutput3::CheckOverlaySupport](..\dxgi1_3\nf-dxgi1_3-idxgioutput3-checkoverlaysupport.md) | Checks for overlay support. |
| [IDXGIOutput4::CheckOverlayColorSpaceSupport](..\dxgi1_4\nf-dxgi1_4-idxgioutput4-checkoverlaycolorspacesupport.md) | Checks for overlay color space support. |
| [IDXGIOutput5::DuplicateOutput1](..\dxgi1_5\nf-dxgi1_5-idxgioutput5-duplicateoutput1.md) | Allows specifying a list of supported formats for fullscreen surfaces that can be returned by the IDXGIOutputDuplication object. |
| [IDXGIOutput6::CheckHardwareCompositionSupport](..\dxgi1_6\nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport.md) | Notifies applications that hardware stretching is supported. |
| [IDXGIOutput6::GetDesc1](..\dxgi1_6\nf-dxgi1_6-idxgioutput6-getdesc1.md) | Get an extended description of the output that includes color characteristics and connection type. |
| [IDXGIOutput::FindClosestMatchingMode](..\dxgi\nf-dxgi-idxgioutput-findclosestmatchingmode.md) | Finds the display mode that most closely matches the requested display mode. |
| [IDXGIOutput::GetDesc](..\dxgi\nf-dxgi-idxgioutput-getdesc.md) | Get a description of the output. |
| [IDXGIOutput::GetDisplayModeList](..\dxgi\nf-dxgi-idxgioutput-getdisplaymodelist.md) | Gets the display modes that match the requested format and other input options. |
| [IDXGIOutput::GetDisplaySurfaceData](..\dxgi\nf-dxgi-idxgioutput-getdisplaysurfacedata.md) | Gets a copy of the current display surface. |
| [IDXGIOutput::GetFrameStatistics](..\dxgi\nf-dxgi-idxgioutput-getframestatistics.md) | Gets statistics about recently rendered frames. |
| [IDXGIOutput::GetGammaControlCapabilities](..\dxgi\nf-dxgi-idxgioutput-getgammacontrolcapabilities.md) | Gets a description of the gamma-control capabilities. |
| [IDXGIOutput::GetGammaControl](..\dxgi\nf-dxgi-idxgioutput-getgammacontrol.md) | Gets the gamma control settings. |
| [IDXGIOutput::ReleaseOwnership](..\dxgi\nf-dxgi-idxgioutput-releaseownership.md) | Releases ownership of the output. |
| [IDXGIOutput::SetDisplaySurface](..\dxgi\nf-dxgi-idxgioutput-setdisplaysurface.md) | Changes the display mode. |
| [IDXGIOutput::SetGammaControl](..\dxgi\nf-dxgi-idxgioutput-setgammacontrol.md) | Sets the gamma controls. |
| [IDXGIOutput::TakeOwnership](..\dxgi\nf-dxgi-idxgioutput-takeownership.md) | Takes ownership of an output. |
| [IDXGIOutput::WaitForVBlank](..\dxgi\nf-dxgi-idxgioutput-waitforvblank.md) | Halt a thread until the next vertical blank occurs. |
| [IDXGIOutputDuplication::AcquireNextFrame](..\dxgi1_2\nf-dxgi1_2-idxgioutputduplication-acquirenextframe.md) | Indicates that the application is ready to process the next desktop image. |
| [IDXGIOutputDuplication::GetDesc](..\dxgi1_2\nf-dxgi1_2-idxgioutputduplication-getdesc.md) | Retrieves a description of a duplicated output. This description specifies the dimensions of the surface that contains the desktop image. |
| [IDXGIOutputDuplication::GetFrameDirtyRects](..\dxgi1_2\nf-dxgi1_2-idxgioutputduplication-getframedirtyrects.md) | Gets information about dirty rectangles for the current desktop frame. |
| [IDXGIOutputDuplication::GetFrameMoveRects](..\dxgi1_2\nf-dxgi1_2-idxgioutputduplication-getframemoverects.md) | Gets information about the moved rectangles for the current desktop frame. |
| [IDXGIOutputDuplication::GetFramePointerShape](..\dxgi1_2\nf-dxgi1_2-idxgioutputduplication-getframepointershape.md) | Gets information about the new pointer shape for the current desktop frame. |
| [IDXGIOutputDuplication::MapDesktopSurface](..\dxgi1_2\nf-dxgi1_2-idxgioutputduplication-mapdesktopsurface.md) | Provides the CPU with efficient access to a desktop image if that desktop image is already in system memory. |
| [IDXGIOutputDuplication::ReleaseFrame](..\dxgi1_2\nf-dxgi1_2-idxgioutputduplication-releaseframe.md) | Indicates that the application finished processing the frame. |
| [IDXGIOutputDuplication::UnMapDesktopSurface](..\dxgi1_2\nf-dxgi1_2-idxgioutputduplication-unmapdesktopsurface.md) | Invalidates the pointer to the desktop image that was retrieved by using IDXGIOutputDuplication |
| [IDXGIResource1::CreateSharedHandle](..\dxgi1_2\nf-dxgi1_2-idxgiresource1-createsharedhandle.md) | Creates a handle to a shared resource. You can then use the returned handle with multiple Direct3D devices. |
| [IDXGIResource1::CreateSubresourceSurface](..\dxgi1_2\nf-dxgi1_2-idxgiresource1-createsubresourcesurface.md) | Creates a subresource surface object. |
| [IDXGIResource::GetEvictionPriority](..\dxgi\nf-dxgi-idxgiresource-getevictionpriority.md) | Get the eviction priority. |
| [IDXGIResource::GetSharedHandle](..\dxgi\nf-dxgi-idxgiresource-getsharedhandle.md) | Gets the handle to a shared resource. |
| [IDXGIResource::GetUsage](..\dxgi\nf-dxgi-idxgiresource-getusage.md) | Get the expected resource usage. |
| [IDXGIResource::SetEvictionPriority](..\dxgi\nf-dxgi-idxgiresource-setevictionpriority.md) | Set the priority for evicting the resource from memory. |
| [IDXGISurface1::GetDC](..\dxgi\nf-dxgi-idxgisurface1-getdc.md) | Returns a device context (DC) that allows you to render to a Microsoft DirectX Graphics Infrastructure (DXGI) surface using Windows Graphics Device Interface (GDI). |
| [IDXGISurface1::ReleaseDC](..\dxgi\nf-dxgi-idxgisurface1-releasedc.md) | Releases the GDI device context (DC) that is associated with the current surface and allows you to use Direct3D to render. |
| [IDXGISurface2::GetResource](..\dxgi1_2\nf-dxgi1_2-idxgisurface2-getresource.md) | Gets the parent resource and subresource index that support a subresource surface. |
| [IDXGISurface::GetDesc](..\dxgi\nf-dxgi-idxgisurface-getdesc.md) | Get a description of the surface. |
| [IDXGISurface::Map](..\dxgi\nf-dxgi-idxgisurface-map.md) | Get a pointer to the data contained in the surface, and deny GPU access to the surface. |
| [IDXGISurface::Unmap](..\dxgi\nf-dxgi-idxgisurface-unmap.md) | Invalidate the pointer to the surface retrieved by IDXGISurface |
| [IDXGISwapChain1::GetBackgroundColor](..\dxgi1_2\nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor.md) | Retrieves the background color of the swap chain. |
| [IDXGISwapChain1::GetCoreWindow](..\dxgi1_2\nf-dxgi1_2-idxgiswapchain1-getcorewindow.md) | Retrieves the underlying CoreWindow object for this swap-chain object. |
| [IDXGISwapChain1::GetDesc1](..\dxgi1_2\nf-dxgi1_2-idxgiswapchain1-getdesc1.md) | Gets a description of the swap chain. |
| [IDXGISwapChain1::GetFullscreenDesc](..\dxgi1_2\nf-dxgi1_2-idxgiswapchain1-getfullscreendesc.md) | Gets a description of a full-screen swap chain. |
| [IDXGISwapChain1::GetHwnd](..\dxgi1_2\nf-dxgi1_2-idxgiswapchain1-gethwnd.md) | Retrieves the underlying HWND for this swap-chain object. |
| [IDXGISwapChain1::GetRestrictToOutput](..\dxgi1_2\nf-dxgi1_2-idxgiswapchain1-getrestricttooutput.md) | Gets the output (the display monitor) to which you can restrict the contents of a present operation. |
| [IDXGISwapChain1::GetRotation](..\dxgi1_2\nf-dxgi1_2-idxgiswapchain1-getrotation.md) | Gets the rotation of the back buffers for the swap chain. |
| [IDXGISwapChain1::IsTemporaryMonoSupported](..\dxgi1_2\nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported.md) | Determines whether a swap chain supports “temporary mono.” |
| [IDXGISwapChain1::Present1](..\dxgi1_2\nf-dxgi1_2-idxgiswapchain1-present1.md) | Presents a frame on the display screen. |
| [IDXGISwapChain1::SetBackgroundColor](..\dxgi1_2\nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor.md) | Changes the background color of the swap chain. |
| [IDXGISwapChain1::SetRotation](..\dxgi1_2\nf-dxgi1_2-idxgiswapchain1-setrotation.md) | Sets the rotation of the back buffers for the swap chain. |
| [IDXGISwapChain2::GetFrameLatencyWaitableObject](..\dxgi1_3\nf-dxgi1_3-idxgiswapchain2-getframelatencywaitableobject.md) | Returns a waitable handle that signals when the DXGI adapter has finished presenting a new frame. |
| [IDXGISwapChain2::GetMatrixTransform](..\dxgi1_3\nf-dxgi1_3-idxgiswapchain2-getmatrixtransform.md) | Gets the transform matrix that will be applied to a composition swap chain upon the next present. |
| [IDXGISwapChain2::GetMaximumFrameLatency](..\dxgi1_3\nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency.md) | Gets the number of frames that the swap chain is allowed to queue for rendering. |
| [IDXGISwapChain2::GetSourceSize](..\dxgi1_3\nf-dxgi1_3-idxgiswapchain2-getsourcesize.md) | Gets the source region used for the swap chain. |
| [IDXGISwapChain2::SetMatrixTransform](..\dxgi1_3\nf-dxgi1_3-idxgiswapchain2-setmatrixtransform.md) | Sets the transform matrix that will be applied to a composition swap chain upon the next present. |
| [IDXGISwapChain2::SetMaximumFrameLatency](..\dxgi1_3\nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency.md) | Sets the number of frames that the swap chain is allowed to queue for rendering. |
| [IDXGISwapChain2::SetSourceSize](..\dxgi1_3\nf-dxgi1_3-idxgiswapchain2-setsourcesize.md) | Sets the source region to be used for the swap chain. |
| [IDXGISwapChain3::CheckColorSpaceSupport](..\dxgi1_4\nf-dxgi1_4-idxgiswapchain3-checkcolorspacesupport.md) | Checks the swap chain's support for color space. |
| [IDXGISwapChain3::GetCurrentBackBufferIndex](..\dxgi1_4\nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex.md) | Gets the index of the swap chain's current back buffer. |
| [IDXGISwapChain3::ResizeBuffers1](..\dxgi1_4\nf-dxgi1_4-idxgiswapchain3-resizebuffers1.md) | Changes the swap chain's back buffer size, format, and number of buffers, where the swap chain was created using a D3D12 command queue as an input device. This should be called when the application window is resized. |
| [IDXGISwapChain3::SetColorSpace1](..\dxgi1_4\nf-dxgi1_4-idxgiswapchain3-setcolorspace1.md) | Sets the color space used by the swap chain. |
| [IDXGISwapChain4::SetHDRMetaData](..\dxgi1_5\nf-dxgi1_5-idxgiswapchain4-sethdrmetadata.md) | This method sets High Dynamic Range (HDR) and Wide Color Gamut (WCG) header metadata. |
| [IDXGISwapChain::GetBuffer](..\dxgi\nf-dxgi-idxgiswapchain-getbuffer.md) | Accesses one of the swap-chain's back buffers. |
| [IDXGISwapChain::GetContainingOutput](..\dxgi\nf-dxgi-idxgiswapchain-getcontainingoutput.md) | Get the output (the display monitor) that contains the majority of the client area of the target window. |
| [IDXGISwapChain::GetDesc](..\dxgi\nf-dxgi-idxgiswapchain-getdesc.md) | Get a description of the swap chain. |
| [IDXGISwapChain::GetFrameStatistics](..\dxgi\nf-dxgi-idxgiswapchain-getframestatistics.md) | Gets performance statistics about the last render frame. |
| [IDXGISwapChain::GetFullscreenState](..\dxgi\nf-dxgi-idxgiswapchain-getfullscreenstate.md) | Get the state associated with full-screen mode. |
| [IDXGISwapChain::GetLastPresentCount](..\dxgi\nf-dxgi-idxgiswapchain-getlastpresentcount.md) | Gets the number of times that IDXGISwapChain |
| [IDXGISwapChain::Present](..\dxgi\nf-dxgi-idxgiswapchain-present.md) | Presents a rendered image to the user. |
| [IDXGISwapChain::ResizeBuffers](..\dxgi\nf-dxgi-idxgiswapchain-resizebuffers.md) | Changes the swap chain's back buffer size, format, and number of buffers. This should be called when the application window is resized. |
| [IDXGISwapChain::ResizeTarget](..\dxgi\nf-dxgi-idxgiswapchain-resizetarget.md) | Resizes the output target. |
| [IDXGISwapChain::SetFullscreenState](..\dxgi\nf-dxgi-idxgiswapchain-setfullscreenstate.md) | Sets the display state to windowed or full screen. |
| [IDXGISwapChainMedia::CheckPresentDurationSupport](..\dxgi1_3\nf-dxgi1_3-idxgiswapchainmedia-checkpresentdurationsupport.md) | Queries the graphics driver for a supported frame present duration corresponding to a custom refresh rate. |
| [IDXGISwapChainMedia::GetFrameStatisticsMedia](..\dxgi1_3\nf-dxgi1_3-idxgiswapchainmedia-getframestatisticsmedia.md) | Queries the system for a DXGI_FRAME_STATISTICS_MEDIA structure that indicates whether a custom refresh rate is currently approved by the system. |
| [IDXGISwapChainMedia::SetPresentDuration](..\dxgi1_3\nf-dxgi1_3-idxgiswapchainmedia-setpresentduration.md) | Requests a custom presentation duration (custom refresh rate). |
