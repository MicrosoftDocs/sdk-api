---
UID: NF:d3d11.D3D11CreateDeviceAndSwapChain
title: D3D11CreateDeviceAndSwapChain function (d3d11.h)
description: Creates a device that represents the display adapter and a swap chain used for rendering.
helpviewer_keywords: ["7e7df363-d5a2-5b79-817f-3e1d6053d170","D3D11CreateDeviceAndSwapChain","D3D11CreateDeviceAndSwapChain function [Direct3D 11]","d3d11/D3D11CreateDeviceAndSwapChain","direct3d11.d3d11createdeviceandswapchain"]
old-location: direct3d11\d3d11createdeviceandswapchain.htm
tech.root: direct3d11
ms.assetid: 84d73e8c-f13c-4343-91de-57f9f8a0ad96
ms.date: 12/05/2018
ms.keywords: 7e7df363-d5a2-5b79-817f-3e1d6053d170, D3D11CreateDeviceAndSwapChain, D3D11CreateDeviceAndSwapChain function [Direct3D 11], d3d11/D3D11CreateDeviceAndSwapChain, direct3d11.d3d11createdeviceandswapchain
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11CreateDeviceAndSwapChain
 - d3d11/D3D11CreateDeviceAndSwapChain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D11.dll
api_name:
 - D3D11CreateDeviceAndSwapChain
---

# D3D11CreateDeviceAndSwapChain function


## -description

Creates a device that represents the display adapter and a swap chain used for rendering.

## -parameters

### -param pAdapter [in, optional]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>*</b>

A pointer to the video adapter to use when creating a <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-intro">device</a>. Pass <b>NULL</b> to use the default adapter, which is the first adapter enumerated
            by <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters">IDXGIFactory1::EnumAdapters</a>. 

<div class="alert"><b>Note</b>  Do not mix the use of DXGI 1.0 (<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>) and DXGI 1.1 (<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a>) in an application. Use <b>IDXGIFactory</b> or <b>IDXGIFactory1</b>, but not both in an application.
            </div>
<div> </div>

### -param DriverType

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE</a></b>

The <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE</a>, which represents the driver type to create.

### -param Software

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HMODULE</a></b>

A handle to a DLL that implements a software rasterizer.
            If <i>DriverType</i> is <i>D3D_DRIVER_TYPE_SOFTWARE</i>, <i>Software</i> must not be <b>NULL</b>. Get the handle by
            calling <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>,
            <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a> ,
            or <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>. The value should be non-<b>NULL</b> when <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE</a> is <b>D3D_DRIVER_TYPE_SOFTWARE</b> and <b>NULL</b> otherwise.

### -param Flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The runtime <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">layers</a> to enable (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_FLAG</a>);
            values can be bitwise OR'd together.

### -param pFeatureLevels [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>s, which determine the order of feature levels to attempt to create.
              If <i>pFeatureLevels</i> is set to <b>NULL</b>,
              this function uses the following array of feature levels:
            


```

{
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1,
};
          
```


<div class="alert"><b>Note</b>  If the Direct3D 11.1 runtime is present on the computer and <i>pFeatureLevels</i> is set to <b>NULL</b>, this function won't create a <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL_11_1</a> device. To create a <b>D3D_FEATURE_LEVEL_11_1</b> device, you must explicitly provide a <b>D3D_FEATURE_LEVEL</b> array that includes <b>D3D_FEATURE_LEVEL_11_1</b>. If you provide a <b>D3D_FEATURE_LEVEL</b> array that contains <b>D3D_FEATURE_LEVEL_11_1</b> on a computer that doesn't have the Direct3D 11.1 runtime installed, this function immediately fails with E_INVALIDARG.
            </div>
<div> </div>

### -param FeatureLevels

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of elements in <i>pFeatureLevels</i>.

### -param SDKVersion

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The SDK version; use <i>D3D11_SDK_VERSION</i>.

### -param pSwapChainDesc [in, optional]

Type: <b>const <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc">DXGI_SWAP_CHAIN_DESC</a>*</b>

A pointer to a swap chain description (see <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc">DXGI_SWAP_CHAIN_DESC</a>) that contains initialization parameters for the swap chain.

### -param ppSwapChain [out, optional]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>**</b>

Returns the address of a pointer to the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a> object that represents the swap chain used for rendering.

### -param ppDevice [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>**</b>

Returns the address of a pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> object that represents the device created. If this parameter is  <b>NULL</b>, no ID3D11Device will be returned'.

### -param pFeatureLevel [out, optional]

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>*</b>

Returns a pointer to a <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>, which represents the first element in an array of feature levels supported
            by the device. Supply <b>NULL</b> as an input if you don't need to determine which feature level is supported.

### -param ppImmediateContext [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>**</b>

Returns the address of a pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> object that represents the device context. If this parameter is <b>NULL</b>, no ID3D11DeviceContext will be returned.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method can return one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.
          

This method returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a> if you call it in a Session 0 process.
          

This method returns E_INVALIDARG if you set the <i>pAdapter</i> parameter to a non-<b>NULL</b> value and the <i>DriverType</i> parameter to the D3D_DRIVER_TYPE_HARDWARE value.
          

This method returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_SDK_COMPONENT_MISSING</a> if you specify <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_DEBUG</a> in <i>Flags</i> and the incorrect version of the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a> is installed on your computer. Install the latest Windows SDK to get the correct version.

## -remarks

<div class="alert"><b>Note</b>  If you call this method in a Session 0 process, it returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.
        </div>
<div> </div>
This entry-point is supported by the Direct3D 11 runtime, which is available on Windows 7, Windows Server 2008 R2, and as an update to
          Windows Vista (KB971644).
        

To create a Direct3D 11.1 device (<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a>), which is available on Windows 8, Windows Server 2012, and Windows 7 and Windows Server 2008 R2 with the <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a> installed, you first create a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> with this function, and then call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on the <b>ID3D11Device</b> object to obtain the <b>ID3D11Device1</b> interface.
        

To create a Direct3D 11.2 device (<a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2">ID3D11Device2</a>), which is available on Windows 8.1 and Windows Server 2012 R2, you first create a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> with this function, and then call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on the <b>ID3D11Device</b> object to obtain the <b>ID3D11Device2</b> interface.
        

Also, see the remarks section in <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a> for details about input parameter dependencies. To create a device without
          creating a swap chain, use the <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a> function.
        

If you set the <i>pAdapter</i> parameter to a non-<b>NULL</b> value, you must also set the <i>DriverType</i> parameter to the D3D_DRIVER_TYPE_UNKNOWN value. If you set the <i>pAdapter</i> parameter to a non-<b>NULL</b> value and the <i>DriverType</i> parameter to the D3D_DRIVER_TYPE_HARDWARE value, <b>D3D11CreateDeviceAndSwapChain</b> returns an <a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a> of E_INVALIDARG.
        

The function signature PFN_D3D11_CREATE_DEVICE_AND_SWAP_CHAIN is provided as a typedef, so that you can use dynamic linking techniques (<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>) instead of statically linking.
      

<h3><a id="Usage_notes"></a><a id="usage_notes"></a><a id="USAGE_NOTES"></a>Usage notes</h3>
<div class="alert"><b>Note</b>  The <b>D3D11CreateDeviceAndSwapChain</b> function does not exist for Windows Store apps. Instead, Windows Store apps use the  <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a> function and then use the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a> method.
          </div>
<div> </div>
<div class="alert"><b>Note</b>  This function has not been updated to support recent additional features of swap chain creation. For the most up-to-date swap chain creation methods, refer to the methods of <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a> (including <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">CreateSwapChainForHwnd</a>, <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">CreateSwapChainForCoreWindow</a> and <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">CreateSwapChainForComposition</a>).</div>
<div> </div>
<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-functions">Core Functions</a>