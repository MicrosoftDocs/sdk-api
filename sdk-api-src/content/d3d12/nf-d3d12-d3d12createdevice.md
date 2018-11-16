---
UID: NF:d3d12.D3D12CreateDevice
title: D3D12CreateDevice function
author: windows-sdk-content
description: Creates a device that represents the display adapter.
old-location: direct3d12\d3d12createdevice.htm
tech.root: direct3d12
ms.assetid: F403D730-CBD4-4AE0-86F6-8CE122E82CB4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D12CreateDevice, D3D12CreateDevice function, d3d12/D3D12CreateDevice, direct3d12.d3d12createdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D12.dll
api_name:
 - D3D12CreateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- D3D12CreateDevice
: 
---

# D3D12CreateDevice function


## -description


Creates a device that represents the display adapter.
        


## -parameters




### -param pAdapter [in, optional]

Type: <b>IUnknown*</b>

A pointer to the video adapter to use when creating a <a href="https://msdn.microsoft.com/b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7">device</a>.
            Pass <b>NULL</b> to use the default adapter, which is the first adapter that is enumerated by <a href="https://msdn.microsoft.com/en-us/library/Bb174538(v=VS.85).aspx">IDXGIFactory1::EnumAdapters</a>.
            

<div class="alert"><b>Note</b>  Don't mix the use of DXGI 1.0 (<a href="https://msdn.microsoft.com/en-us/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a>) and DXGI 1.1 (<a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a>) in an application.
              Use <b>IDXGIFactory</b> or <b>IDXGIFactory1</b>, but not both in an application.
            </div>
<div> </div>

### -param MinimumFeatureLevel

Type: <b><a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a></b>

The minimum <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a> required for successful device creation.
            


### -param riid [in]

Type: <b><b>REFIID</b></b>

The globally unique identifier (<b>GUID</b>) for the device interface.
            This parameter, and <i>ppDevice</i>, can be addressed with the single macro
          <a href="https://msdn.microsoft.com/268B59FA-44EB-4777-8162-C50981CBDD09">IID_PPV_ARGS</a>.


### -param ppDevice [out, optional]

Type: <b><b>void</b>**</b>

A pointer to a memory block that receives a pointer to the device.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method can return one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          

Possible return values include those documented for <a href="https://msdn.microsoft.com/6fb9d7a3-0b59-4b7a-8871-b99d59811d46">CreateDXGIFactory1</a> and  <a href="https://msdn.microsoft.com/en-us/library/Bb174538(v=VS.85).aspx">IDXGIFactory::EnumAdapters</a>.
          




## -remarks



In order to be sure to pick up the first adapter that supports D3D12, use the following code. 

<pre class="syntax" xml:space="preserve"><code>void GetHardwareAdapter(IDXGIFactory4* pFactory, IDXGIAdapter1** ppAdapter)
{
    *ppAdapter = nullptr;
    for (UINT adapterIndex = 0; ; ++adapterIndex)
    {
        IDXGIAdapter1* pAdapter = nullptr;
        if (DXGI_ERROR_NOT_FOUND == pFactory-&gt;EnumAdapters1(adapterIndex, &amp;pAdapter))
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
        pAdapter-&gt;Release();
    }
}
</code></pre>
The function signature PFN_D3D12_CREATE_DEVICE is provided as a typedef, so that you can use dynamic linking techniques (<a href="https://msdn.microsoft.com/library/windows/desktop/ms683212(v=vs.85).aspx">GetProcAddress</a>) instead of statically linking.
      

The <b>REFIID</b>, or <b>GUID</b>, of the interface to a device can be obtained by using the<code> __uuidof()</code> macro.
        For example, <code>__uuidof</code>(<a href="https://msdn.microsoft.com/en-us/library/Dn788650(v=VS.85).aspx">ID3D12Device</a>) will get the <b>GUID</b> of the interface to a device.
      


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


Refer to the <a href="https://msdn.microsoft.com/en-us/library/Dn933255(v=VS.85).aspx">Example Code in the D3D12 Reference</a>. 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn770456(v=VS.85).aspx">Core Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt186624(v=VS.85).aspx">Working Samples</a>
 

 

