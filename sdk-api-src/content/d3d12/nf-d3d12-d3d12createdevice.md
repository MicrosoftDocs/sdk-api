---
UID: NF:d3d12.D3D12CreateDevice
title: D3D12CreateDevice function (d3d12.h)
description: Creates a device that represents the display adapter. (D3D12CreateDevice)
helpviewer_keywords: ["D3D12CreateDevice","D3D12CreateDevice function","d3d12/D3D12CreateDevice","direct3d12.d3d12createdevice"]
old-location: direct3d12\d3d12createdevice.htm
tech.root: direct3d12
ms.assetid: F403D730-CBD4-4AE0-86F6-8CE122E82CB4
ms.date: 12/05/2018
ms.keywords: D3D12CreateDevice, D3D12CreateDevice function, d3d12/D3D12CreateDevice, direct3d12.d3d12createdevice
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12CreateDevice
 - d3d12/D3D12CreateDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D12.dll
api_name:
 - D3D12CreateDevice
---

# D3D12CreateDevice function


## -description

Creates a device that represents the display adapter.

## -parameters

### -param pAdapter [in, optional]

Type: <b>IUnknown*</b>

A pointer to the video adapter to use when creating a <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-intro">device</a>.
            Pass <b>NULL</b> to use the default adapter, which is the first adapter that is enumerated by <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters">IDXGIFactory1::EnumAdapters</a>.
            

<div class="alert"><b>Note</b>  Don't mix the use of DXGI 1.0 (<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>) and DXGI 1.1 (<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a>) in an application.
              Use <b>IDXGIFactory</b> or <b>IDXGIFactory1</b>, but not both in an application.
            </div>
<div> </div>

### -param MinimumFeatureLevel

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a></b>

The minimum <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a> required for successful device creation.

### -param riid [in]

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the device interface.
            This parameter, and <i>ppDevice</i>, can be addressed with the single macro
          <a href="/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args">IID_PPV_ARGS</a>.

### -param ppDevice [out, optional]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the device. Pass **NULL** to test if device creation would succeed, but to not actually create the device. If **NULL** is passed and device creation would succeed, **S_FALSE** is returned.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method can return one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.
          

Possible return values include those documented for <a href="/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1">CreateDXGIFactory1</a> and  <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters">IDXGIFactory::EnumAdapters</a>.
          
If **ppDevice** is **NULL** and the function succeeds, **S_FALSE** is returned, rather than **S_OK**.

## -remarks

Direct3D 12 devices are singletons per adapter. If a Direct3D 12 device already exists in the current process for a given adapter, then a subsequent call to **D3D12CreateDevice** returns the existing device. If the current Direct3D 12 device is in a removed state (that is, [ID3D12Device::GetDeviceRemovedReason](nf-d3d12-id3d12device-getdeviceremovedreason.md) returns a failing HRESULT), then **D3D12CreateDevice** fails instead of returning the existing device. The sameness of two adapters (that is, they have the same identity) is determined by comparing their LUIDs, not their pointers.

In order to be sure to pick up the first adapter that supports D3D12, use the following code. 


``` syntax
void GetHardwareAdapter(IDXGIFactory4* pFactory, IDXGIAdapter1** ppAdapter)
{
    *ppAdapter = nullptr;
    for (UINT adapterIndex = 0; ; ++adapterIndex)
    {
        IDXGIAdapter1* pAdapter = nullptr;
        if (DXGI_ERROR_NOT_FOUND == pFactory->EnumAdapters1(adapterIndex, &pAdapter))
        {
            // No more adapters to enumerate.
            break;
        } 

        // Check to see if the adapter supports Direct3D 12, but don't create the
        // actual device yet.
        if (SUCCEEDED(D3D12CreateDevice(pAdapter, D3D_FEATURE_LEVEL_11_0, _uuidof(ID3D12Device), nullptr)))
        {
            *ppAdapter = pAdapter;
            return;
        }
        pAdapter->Release();
    }
}

```

The function signature PFN_D3D12_CREATE_DEVICE is provided as a typedef, so that you can use dynamic linking techniques (<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>) instead of statically linking.
      

The <b>REFIID</b>, or <b>GUID</b>, of the interface to a device can be obtained by using the<code> __uuidof()</code> macro.
        For example, <code>__uuidof</code>(<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>) will get the <b>GUID</b> of the interface to a device.
      


#### Examples

Create a hardware based device, unless instructed to create a WARP software device.
        


```cpp
ComPtr<IDXGIFactory4> factory;
ThrowIfFailed(CreateDXGIFactory1(IID_PPV_ARGS(&factory)));

if (m_useWarpDevice)
{
    ComPtr<IDXGIAdapter> warpAdapter;
    ThrowIfFailed(factory->EnumWarpAdapter(IID_PPV_ARGS(&warpAdapter)));

    ThrowIfFailed(D3D12CreateDevice(
        warpAdapter.Get(),
        D3D_FEATURE_LEVEL_11_0,
        IID_PPV_ARGS(&m_device)
        ));
}
else
{
    ComPtr<IDXGIAdapter1> hardwareAdapter;
    GetHardwareAdapter(factory.Get(), &hardwareAdapter);

    ThrowIfFailed(D3D12CreateDevice(
        hardwareAdapter.Get(),
        D3D_FEATURE_LEVEL_11_0,
        IID_PPV_ARGS(&m_device)
        ));
}

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>. 

<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-functions">Core Functions</a>



<a href="/windows/desktop/direct3d12/working-samples">Working Samples</a>
