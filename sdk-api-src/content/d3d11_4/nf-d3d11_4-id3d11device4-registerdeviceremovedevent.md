---
UID: NF:d3d11_4.ID3D11Device4.RegisterDeviceRemovedEvent
title: ID3D11Device4::RegisterDeviceRemovedEvent (d3d11_4.h)
description: Registers the &quot;device removed&quot; event and indicates when a Direct3D device has become removed for any reason, using an asynchronous notification mechanism.
helpviewer_keywords: ["ID3D11Device4 interface [Direct3D 11]","RegisterDeviceRemovedEvent method","ID3D11Device4.RegisterDeviceRemovedEvent","ID3D11Device4::RegisterDeviceRemovedEvent","RegisterDeviceRemovedEvent","RegisterDeviceRemovedEvent method [Direct3D 11]","RegisterDeviceRemovedEvent method [Direct3D 11]","ID3D11Device4 interface","d3d11_4/ID3D11Device4::RegisterDeviceRemovedEvent","direct3d11.id3d11device4_registerdeviceremovedevent"]
old-location: direct3d11\id3d11device4_registerdeviceremovedevent.htm
tech.root: direct3d11
ms.assetid: 6C564C67-9166-4F65-B099-3DDDECCEDC40
ms.date: 12/05/2018
ms.keywords: ID3D11Device4 interface [Direct3D 11],RegisterDeviceRemovedEvent method, ID3D11Device4.RegisterDeviceRemovedEvent, ID3D11Device4::RegisterDeviceRemovedEvent, RegisterDeviceRemovedEvent, RegisterDeviceRemovedEvent method [Direct3D 11], RegisterDeviceRemovedEvent method [Direct3D 11],ID3D11Device4 interface, d3d11_4/ID3D11Device4::RegisterDeviceRemovedEvent, direct3d11.id3d11device4_registerdeviceremovedevent
req.header: d3d11_4.h
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device4::RegisterDeviceRemovedEvent
 - d3d11_4/ID3D11Device4::RegisterDeviceRemovedEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11Device4.RegisterDeviceRemovedEvent
---

# ID3D11Device4::RegisterDeviceRemovedEvent


## -description

Registers the "device removed" event and indicates when a Direct3D device has become removed for any reason, using an asynchronous notification mechanism.

## -parameters

### -param hEvent [in]

Type: <b>HANDLE</b>

The handle to the "device removed" event.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to information about the "device removed" event, which can be used in <a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved">UnregisterDeviceRemoved</a> to unregister the event.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

See <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

Indicates when a Direct3D device has become removed for any reason, using an asynchronous notification mechanism, rather than as an HRESULT from <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a>. The reason for device removal can be retrieved using <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-getdeviceremovedreason">ID3D11Device::GetDeviceRemovedReason</a> after being notified of the occurrence.

Applications register and un-register a Win32 event handle with a particular device.
          That event handle will be signaled when the device becomes removed.
          A poll into the device's <b>ID3D11Device::GetDeviceRemovedReason</b> method indicates that the device is removed.
        


<a href="/uwp/api/Windows.System.Threading.Core">ISignalableNotifier</a> or <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait">SetThreadpoolWait</a> can be used by UWP apps.
        

When the graphics device is lost, the app or title will receive the graphics event, so that the app or title knows that its graphics device is no longer valid and it is safe for the app or title to re-create its DirectX devices.
          In response to this event, the app or title needs to re-create its rendering device 
			 and pass it into a SetRenderingDevice  call on the composition graphics device objects.
        

After setting this new rendering device, the app or title needs to redraw content of all the pre-existing surfaces 
			 after the composition graphics device's <b>OnRenderingDeviceReplaced</b> event is fired.
        

This method supports Composition for device loss.
        

The event is not signaled when it is most ideal to re-create.
          So, instead, we recommend iterating through the adapter ordinals and creating the first ordinal that will succeed.
        

The application can register an event with the device.
          The application will be signaled when the device becomes removed.
        

If the device is already removed, calls to <b>RegisterDeviceRemovedEvent</b> will signal the event immediately.
          No device-removed error code will be returned from <b>RegisterDeviceRemovedEvent</b>.
        

Each "device removed" event is never signaled, or is signaled only once.
          These events are not signaled during device destruction.
          These events are unregistered during destruction.
        

The semantics of <b>RegisterDeviceRemovedEvent</b> are similar to
          <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent">IDXGIFactory2::RegisterOcclusionStatusEvent</a>.

## -see-also

<a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4">ID3D11Device4</a>



<a href="/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved">UnregisterDeviceRemoved</a>