---
UID: NF:windows.graphics.holographic.interop.IHolographicCameraRenderingParametersInterop.CommitDirect3D12ResourceWithDepthData
title: IHolographicCameraRenderingParametersInterop::CommitDirect3D12ResourceWithDepthData
description: The IHolographicCameraRenderingParametersInterop::CommitDirect3D12ResourceWithDepthData function commits a Direct3D 12 buffer for HolographicCamera outputs.
tech.root: direct3d12
ms.date: 08/03/2022
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: windows.graphics.holographic.interop.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - windows.graphics.holographic.interop.h
api_name:
 - IHolographicCameraRenderingParametersInterop::CommitDirect3D12ResourceWithDepthData
f1_keywords:
 - IHolographicCameraRenderingParametersInterop::CommitDirect3D12ResourceWithDepthData
 - windows.graphics.holographic.interop/IHolographicCameraRenderingParametersInterop::CommitDirect3D12ResourceWithDepthData
dev_langs:
 - c++
---

## -description

Commits a Direct3D 12 buffer for presentation on outputs associated with the [HolographicCamera](/uwp/api/windows.graphics.holographic.holographiccamera). The buffer must have been created by calling [CreateDirect3D12BackBufferResource](./nf-windows-graphics-holographic-interop-iholographiccamerainterop-createdirect3d12backbufferresource.md) or [CreateDirect3D12HardwareProtectedBackBufferResource](nf-windows-graphics-holographic-interop-iholographiccamerainterop-createdirect3d12hardwareprotectedbackbufferresource.md) on the same [HolographicCamera](/uwp/api/windows.graphics.holographic.holographiccamera) that it is committed for.

This method also accepts an optional depth buffer parameter, along with fence and fence value for app work completion on that buffer. This depth buffer will be used for image stabilization when showing the frame it is committed to. The depth buffer must contain depth data correlated with geometry used to draw holograms in the color buffer, which is submitted at the same time. The depth buffer should not contain depth data for invisible content, such as depth data used for occlusion.

## -parameters

### -param pColorResourceToCommit

Type: **[ID3D12Resource](../d3d12/nn-d3d12-id3d12resource.md)\***

The Direct3D 12 texture resource with content to display when presenting the [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe) used to retrieve this rendering parameters object.

### -param pColorResourceFence

Type: **[ID3D12Fence](../d3d12/nn-d3d12-id3d12fence.md)\***

A fence used to signal app work completion on the color buffer resource indicated by *pColorResourceToCommit*. Completion of this fence at the value indicated by *colorResourceFenceSignalValue* signals transfer of control of the color resource from your application to the platform in the GPU work queue. The platform relies upon this fence, and the value indicated in *colorResourceFenceSignalValue*, to queue work on the GPU that reads from the color buffer.

### -param colorResourceFenceSignalValue

Type: **[UINT64](/windows/win32/winprog/windows-data-types)**

The value used to signal work completion on *pColorResourceFence*. The platform relies upon this fence value to queue work on the GPU that reads from the color buffer.

### -param pDepthResourceToCommit

Type: **[ID3D12Resource](../d3d12/nn-d3d12-id3d12resource.md)\***

The Direct3D 12 depth buffer with depth data to use for image stabilization when presenting the [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe) used to retrieve this rendering parameters object. Applications typically submit the depth stencil used when rendering to *pColorResourceToCommit*, or a depth buffer that is derived from the same rendering pass. The depth buffer should only include data corresponding to geometry used to render holograms in the color buffer; for example, occlusion data shouldn't be included, and may be ignored by the platform.

### -param pDepthResourceFence

Type: **[ID3D12Fence](../d3d12/nn-d3d12-id3d12fence.md)\***

A fence used to signal work completion on the depth buffer resource indicated by *pDepthResourceToCommit*. Completion of this fence at the value indicated by *depthResourceFenceSignalValue* signals transfer of control of the depth resource from your application to the platform in the GPU work queue. The platform relies upon this fence, and the value indicated in *colorResourceFenceSignalValue*, to queue work on the GPU that reads from the depth buffer.

### -param depthResourceFenceSignalValue

Type: **[UINT64](/windows/win32/winprog/windows-data-types)**

The value used to signal work completion on *pDepthResourceFence*. The platform relies upon this fence value to queue work on the GPU that reads from the depth buffer.

## -returns

**S_OK** if successful, otherwise returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) error code indicating the reason for failure. Also see [COM Error Codes (UI, Audio, DirectX, Codec)](/windows/win32/com/com-error-codes-10).

## -see-also
