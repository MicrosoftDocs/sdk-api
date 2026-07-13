---
UID: NF:d3d11.D3D11CreateDevice
title: D3D11CreateDevice function (d3d11.h)
description: Creates a device that represents the display adapter. (D3D11CreateDevice)
helpviewer_keywords: ["763ee631-eef7-d99f-1d0d-58e3651843f9","D3D11CreateDevice","D3D11CreateDevice function [Direct3D 11]","d3d11/D3D11CreateDevice","direct3d11.d3d11createdevice"]
old-location: direct3d11\d3d11createdevice.htm
tech.root: direct3d11
ms.assetid: d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b
ms.date: 12/05/2018
ms.keywords: 763ee631-eef7-d99f-1d0d-58e3651843f9, D3D11CreateDevice, D3D11CreateDevice function [Direct3D 11], d3d11/D3D11CreateDevice, direct3d11.d3d11createdevice
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
 - D3D11CreateDevice
 - d3d11/D3D11CreateDevice
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
 - D3D11CreateDevice
---

# D3D11CreateDevice function


## -description

Creates a device that represents the display adapter.

## -parameters

### -param pAdapter [in, optional]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>*</b>

A pointer to the video adapter to use when creating a <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-intro">device</a>. Pass <b>NULL</b> to use the default adapter, which is the first adapter that is enumerated by <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters">IDXGIFactory1::EnumAdapters</a>. 

<div class="alert"><b>Note</b>  Do not mix the use of DXGI 1.0 (<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>) and DXGI 1.1 (<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a>) in an application. Use <b>IDXGIFactory</b> or <b>IDXGIFactory1</b>, but not both in an application.
            </div>
<div> </div>

### -param DriverType

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE</a></b>

The <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type">D3D_DRIVER_TYPE</a>, which represents the driver type to create.

### -param Software

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HMODULE</a></b>

A handle to a DLL that implements a software rasterizer.
            If <i>DriverType</i> is <i>D3D_DRIVER_TYPE_SOFTWARE</i>,
            <i>Software</i> must not be <b>NULL</b>. Get the handle by
            calling <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>,
            <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a> ,
            or <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>.

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

### -param ppDevice [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>**</b>

Returns the address of a pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> object that represents the device created. If this parameter is <b>NULL</b>, no ID3D11Device will be returned.

### -param pFeatureLevel [out, optional]

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>*</b>

If successful, returns the first <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a> from the <i>pFeatureLevels</i> array which succeeded. Supply <b>NULL</b> as an input if you don't need to determine which feature level is supported.

### -param ppImmediateContext [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>**</b>

Returns the address of a pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> object that represents the device context. If this parameter is <b>NULL</b>, no ID3D11DeviceContext will be returned.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method can return one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.
          

This method returns E_INVALIDARG if you set the <i>pAdapter</i> parameter to a non-<b>NULL</b> value and the <i>DriverType</i> parameter to the D3D_DRIVER_TYPE_HARDWARE value.
          

This method returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_SDK_COMPONENT_MISSING</a> if you specify <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_DEBUG</a> in <i>Flags</i> and the incorrect version of the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a> is installed on your computer. Install the latest Windows SDK to get the correct version.

## -remarks

This entry-point is supported by the Direct3D 11 runtime, which is available on Windows 7, Windows Server 2008 R2, and as an update to
          Windows Vista (KB971644).
        

To create a Direct3D 11.1 device (<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a>), which is available on Windows 8, Windows Server 2012, and Windows 7 and Windows Server 2008 R2 with the <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a> installed, you first create a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> with this function, and then call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on the <b>ID3D11Device</b> object to obtain the <b>ID3D11Device1</b> interface.
        

To create a Direct3D 11.2 device (<a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2">ID3D11Device2</a>), which is available on Windows 8.1 and Windows Server 2012 R2, you first create a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> with this function, and then call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on the <b>ID3D11Device</b> object to obtain the <b>ID3D11Device2</b> interface.
        

Set <i>ppDevice</i> and <i>ppImmediateContext</i> to <b>NULL</b> to determine which feature level is supported by looking
          at <i>pFeatureLevel</i> without creating a device.
        

For an example, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-initialize">How To: Create a Device and Immediate Context</a>; to create a device and a swap chain at the same time,
          use <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain">D3D11CreateDeviceAndSwapChain</a>.
        

If you set the <i>pAdapter</i> parameter to a non-<b>NULL</b> value, you must also set the <i>DriverType</i> parameter to the D3D_DRIVER_TYPE_UNKNOWN value. If you set the <i>pAdapter</i> parameter to a non-<b>NULL</b> value and the <i>DriverType</i> parameter to the D3D_DRIVER_TYPE_HARDWARE value, <b>D3D11CreateDevice</b> returns an <a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a> of E_INVALIDARG.
        

<table>
<tr>
<td>
Differences between Direct3D 10 and Direct3D 11:

In Direct3D 10, the presence of <i>pAdapter</i> dictated which adapter to use and the <i>DriverType</i> could
                mismatch what the adapter was.
              

In Direct3D 11, if you are trying to create a hardware or a software device, set <i>pAdapter</i> != <b>NULL</b> which constrains
                the other inputs to be:
              

<ul>
<li><i>DriverType</i> must be D3D_DRIVER_TYPE_UNKNOWN
                </li>
<li><i>Software</i> must be <b>NULL</b>.
                </li>
</ul>
On the other hand, if <i>pAdapter</i> == <b>NULL</b>, the <i>DriverType</i> cannot be set to D3D_DRIVER_TYPE_UNKNOWN; it can be set to either:
              

<ul>
<li>If <i>DriverType</i> == D3D_DRIVER_TYPE_SOFTWARE,  <i>Software</i> cannot be <b>NULL</b>.
                </li>
<li>If <i>DriverType</i> == D3D_DRIVER_TYPE_HARDWARE, the adapter used will be the default adapter, which is the first adapter that is enumerated by <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters">IDXGIFactory1::EnumAdapters</a>
</li>
</ul>
</td>
</tr>
</table>
 

The function signature PFN_D3D11_CREATE_DEVICE is provided as a typedef, so that you can use dynamic linking techniques (<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>) instead of statically linking.
      

<b>Windows Phone 8:
        </b> This API is supported.
      

<b>Windows Phone 8.1:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-functions">Core Functions</a>
