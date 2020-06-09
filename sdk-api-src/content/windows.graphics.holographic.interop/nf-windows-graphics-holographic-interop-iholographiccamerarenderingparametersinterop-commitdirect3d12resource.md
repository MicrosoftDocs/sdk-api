---
UID: NF:windows.graphics.holographic.interop.IHolographicCameraRenderingParametersInterop.CommitDirect3D12Resource
title: IHolographicCameraRenderingParametersInterop::CommitDirect3D12Resource
description: Commits a Direct3D 12 buffer for presentation on outputs associated with the [HolographicCamera](/uwp/api/windows.graphics.holographic.holographiccamera).
tech.root: direct3d12
ms.date: 12/12/2019
ms.topic: language-reference
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
 - IHolographicCameraRenderingParametersInterop::CommitDirect3D12Resource
f1_keywords:
 - windows/IHolographicCameraRenderingParametersInterop::CommitDirect3D12Resource
dev_langs:
 - c++
---

## -description
The **CommitDirect3D12Resource** method commits a Direct3D 12 buffer for presentation on outputs associated with a [HolographicCamera](/uwp/api/windows.graphics.holographic.holographiccamera) during a specific [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe). The buffer must have been created by calling [CreateDirect3D12BackBufferResource](/windows/win32/api/windows.graphics.holographic.interop/nf-windows-graphics-holographic-interop-iholographiccamerainterop-createdirect3d12backbufferresource) or [CreateDirect3D12HardwareProtectedBackBufferResource](nf-windows-graphics-holographic-interop-iholographiccamerainterop-createdirect3d12hardwareprotectedbackbufferresource.md) on the same [HolographicCamera](/uwp/api/windows.graphics.holographic.holographiccamera) corresponding to this rendering parameters object, and the buffer must have been acquired by your application prior to rendering.

## -parameters

### -param pColorResourceToCommit
Type: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***

The Direct3D 12 texture resource with content to display when presenting the [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe) used to retrieve this rendering parameters object.

### -param pColorResourceFence
Type: **[ID3D12Fence](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)\***

A fence used to signal app work completion on the color buffer resource indicated by *pColorResourceToCommit*. Completion of this fence at the value indicated by *colorResourceFenceSignalValue* signals transfer of control of the color resource from your application to the platform in the GPU work queue. The platform relies upon this fence, and the value indicated in *colorResourceFenceSignalValue*, to queue work on the GPU that reads from the color buffer.

### -param colorResourceFenceSignalValue
Type: **[UINT64](/windows/win32/winprog/windows-data-types)**

The value used to signal work completion on *pColorResourceFence*. The platform relies upon this fence value to queue work on the GPU that reads from the color buffer.

## -returns
**S_OK** if successful, otherwise returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) error code indicating the  reason for failure. Also see [COM Error Codes (UI, Audio, DirectX, Codec)](/windows/win32/com/com-error-codes-10).

## -see-also
