---
UID: NF:windows.graphics.holographic.interop.IHolographicCameraInterop.AcquireDirect3D12BufferResourceWithTimeout
title: IHolographicCameraInterop::AcquireDirect3D12BufferResourceWithTimeout
description: The IHolographicCameraInterop::AcquireDirect3D12BufferResourceWithTimeout function acquires a Direct3D 12 buffer resource, with an optional timeout.
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
 - IHolographicCameraInterop::AcquireDirect3D12BufferResourceWithTimeout
f1_keywords:
 - IHolographicCameraInterop::AcquireDirect3D12BufferResourceWithTimeout
 - windows.graphics.holographic.interop/IHolographicCameraInterop::AcquireDirect3D12BufferResourceWithTimeout
dev_langs:
 - c++
---

## -description

The **AcquireDirect3D12BufferResourceWithTimeout** method transitions ownership of a Direct3D 12 back buffer resource from the platform to your application, waiting up to the amount of time indicated by the *duration* argument for the resource to become available. If your application already owns control of the resource, the acquisition is considered to be a success, and the method returns immediately.

After committing a resource to a [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe) by calling [IHolographicQuadLayerUpdateParametersInterop::CommitDirect3D12Resource](./nf-windows-graphics-holographic-interop-iholographicquadlayerupdateparametersinterop-commitdirect3d12resource.md), your application should consider control of that resource to be owned by the system until such a time as it is reacquired by your application using **AcquireDirect3D12BufferResourceWithTimeout**. The system owns the buffer until the frame that the buffer was committed to makes its way through the presentation queue. To determine whether the system has relinquished control of the buffer, call  **AcquireDirect3D12BufferResource** or **AcquireDirect3D12BufferResourceWithTimeout**. If the buffer can't be acquired by the time your application is ready to start rendering a new [HolographicFrame](/uwp/api/windows.graphics.holographic.holographicframe), then you should create a new resource and add it to the buffer queue, or limit the queue size by waiting for a buffer to become available.

This method accepts an optional timeout value. When a nonzero value is present in the *duration* argument, the system waits for that many milliseconds for the buffer to become available. The default behavior is to not wait. When a timeout value of zero is specified and the buffer is not ready to be acquired, the method call fails with the error code **E_NOTREADY**.

## -parameters

### -param pResourceToAcquire

Type: **[ID3D12Resource](../d3d12/nn-d3d12-id3d12resource.md)\***

The Direct3D 12 resource to acquire.

### -param pCommandQueue

Type: **[ID3D12CommandQueue](../d3d12/nn-d3d12-id3d12commandqueue.md)\***

The Direct3D 12 command queue to use for transitioning the state of this resource when acquiring it for your application. The resource will be in the **D3D12_RESOURCE_STATE_COMMON** state when it is acquired.

### -param duration

Type: **[UINT64](/windows/win32/winprog/windows-data-types)**

If this parameter is set to a non-zero value, the call will wait for that amount of time for the buffer to be acquired. If the timeout period elapses before the buffer can be acquired, the method will fail with the error code **E_TIMEOUT**. This parameter is specified in 100-nanosecond units, similar to the [TimeSpan.Duration](/uwp/api/windows.foundation.timespan.duration) field.

## -returns

**S_OK** if successful, otherwise returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) error code indicating the reason for failure. Also see [COM Error Codes (UI, Audio, DirectX, Codec)](/windows/win32/com/com-error-codes-10).

## -see-also
