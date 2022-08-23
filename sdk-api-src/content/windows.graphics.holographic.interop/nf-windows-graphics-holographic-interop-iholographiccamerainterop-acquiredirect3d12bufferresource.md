---
UID: NF:windows.graphics.holographic.interop.IHolographicCameraInterop.AcquireDirect3D12BufferResource
title: IHolographicCameraInterop::AcquireDirect3D12BufferResource
description: The IHolographicCameraInterop::AcquireDirect3D12BufferResource function acquires a Direct3D 12 buffer resource.
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
 - IHolographicCameraInterop::AcquireDirect3D12BufferResource
f1_keywords:
 - IHolographicCameraInterop::AcquireDirect3D12BufferResource
 - windows.graphics.holographic.interop/IHolographicCameraInterop::AcquireDirect3D12BufferResource
dev_langs:
 - c++
---

## -description

The **AcquireDirect3D12BufferResource** method transitions ownership of a Direct3D 12 back buffer resource from the platform to your application. If your application already owns control of the resource, then the acquisition is still considered to be a success.

After committing a resource to a [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe) by calling [IHolographicQuadLayerUpdateParametersInterop::CommitDirect3D12Resource](/windows/win32/api/windows.graphics.holographic.interop/nn-windows-graphics-holographic-interop-iholographicquadlayerupdateparametersinterop), your application should consider control of that resource to be owned by the system until such a time as the resource is reacquired by your application using this method. The system owns the buffer until the frame that the buffer was committed to makes its way through the presentation queue. To determine whether the system has relinquished control of the buffer, call  **AcquireDirect3D12BufferResource** or **AcquireDirect3D12BufferResourceWithTimeout**. If the buffer can't be acquired by the time your application is ready to start rendering a new [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe), then you should create a new resource and add it to the buffer queue, or limit the queue size by waiting for a buffer to become available.

If the buffer isn't ready to be acquired when **AcquireDirect3D12BufferResource** is called, then the method call will fail and immediately return the error code **E_NOTREADY**.

Your application can limit the queue size by calling [AcquireDirect3D12BufferResourceWithTimeout](./nf-windows-graphics-holographic-interop-iholographiccamerainterop-acquiredirect3d12bufferresourcewithtimeout.md) to wait until a resource becomes available before queuing more work.

## -parameters

### -param pResourceToAcquire

Type: **[ID3D12Resource](../d3d12/nn-d3d12-id3d12resource.md)\***

The Direct3D 12 resource to acquire.

### -param pCommandQueue

Type: **[ID3D12CommandQueue](../d3d12/nn-d3d12-id3d12commandqueue.md)\***

The Direct3D 12 command queue to use for transitioning the state of this resource when acquiring it for your application.
The resource will be in the **D3D12_RESOURCE_STATE_COMMON** state when it is acquired. The resource transition command may not be queued if the resource is already in the common state when it is being acquired.

## -returns

**S_OK** if successful, otherwise returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) error code indicating the reason for failure. Also see [COM Error Codes (UI, Audio, DirectX, Codec)](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
