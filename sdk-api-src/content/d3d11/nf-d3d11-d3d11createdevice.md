---
UID: NF:d3d11.D3D11CreateDevice
title: D3D11CreateDevice function
author: windows-sdk-content
description: Creates a device that represents the display adapter.
old-location: direct3d11\d3d11createdevice.htm
old-project: direct3d11
ms.assetid: d1c85ec0-84a8-41ff-9cbe-f47bbaa5863b
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 763ee631-eef7-d99f-1d0d-58e3651843f9, D3D11CreateDevice, D3D11CreateDevice function [Direct3D 11], d3d11/D3D11CreateDevice, direct3d11.d3d11createdevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	D3D11.dll
api_name:
-	D3D11CreateDevice
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
---

# D3D11CreateDevice function


## -description


Creates a device that represents the display adapter.


## -parameters




### -param pAdapter [in, optional]

Type: <b><a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>*</b>


            A pointer to the video adapter to use when creating a <a href="https://msdn.microsoft.com/b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7">device</a>. Pass <b>NULL</b> to use the default adapter, which is the first adapter that is enumerated by <a href="https://msdn.microsoft.com/23e876c7-b32a-4bc9-84c1-9e8949680e14">IDXGIFactory1::EnumAdapters</a>. 

<div class="alert"><b>Note</b>  
              Do not mix the use of DXGI 1.0 (<a href="https://msdn.microsoft.com/642aac36-ca5a-4c62-b5cb-f9d35965ca2f">IDXGIFactory</a>) and DXGI 1.1 (<a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a>) in an application. Use <b>IDXGIFactory</b> or <b>IDXGIFactory1</b>, but not both in an application.
            </div>
<div> </div>

### -param DriverType

Type: <b><a href="https://msdn.microsoft.com/ceeec7d6-4bdc-488c-80a8-6c5e11986d6a">D3D_DRIVER_TYPE</a></b>


            The <a href="https://msdn.microsoft.com/ceeec7d6-4bdc-488c-80a8-6c5e11986d6a">D3D_DRIVER_TYPE</a>, which represents the driver type to create.
          


### -param Software

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMODULE</a></b>


            A handle to a DLL that implements a software rasterizer.
            If <i>DriverType</i> is <i>D3D_DRIVER_TYPE_SOFTWARE</i>,
            <i>Software</i> must not be <b>NULL</b>. Get the handle by
            calling <a href="http://msdn.microsoft.com/en-us/library/ms684175.aspx">LoadLibrary</a>,
            <a href="http://msdn.microsoft.com/en-us/library/ms684179.aspx">LoadLibraryEx</a> ,
            or <a href="http://msdn.microsoft.com/en-us/library/ms683199.aspx">GetModuleHandle</a>.
          


### -param Flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            The runtime <a href="https://msdn.microsoft.com/c545983c-5351-42a9-82e5-deea73aa035f">layers</a> to enable (see <a href="https://msdn.microsoft.com/580c784a-17de-495c-9159-833f858ad155">D3D11_CREATE_DEVICE_FLAG</a>);
            values can be bitwise OR'd together.
          


### -param pFeatureLevels [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a>*</b>


              A pointer to an array of <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a>s, which determine the order of feature levels to attempt to create.
              If <i>pFeatureLevels</i> is set to <b>NULL</b>,
              this function uses the following array of feature levels:
            

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>{
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1,
};</pre>
</td>
</tr>
</table></span></div>
<div class="alert"><b>Note</b>  
              If the Direct3D 11.1 runtime is present on the computer and <i>pFeatureLevels</i> is set to <b>NULL</b>, this function won't create a <a href="d3d_feature_level.htm">D3D_FEATURE_LEVEL_11_1</a> device. To create a <b>D3D_FEATURE_LEVEL_11_1</b> device, you must explicitly provide a <b>D3D_FEATURE_LEVEL</b> array that includes <b>D3D_FEATURE_LEVEL_11_1</b>. If you provide a <b>D3D_FEATURE_LEVEL</b> array that contains <b>D3D_FEATURE_LEVEL_11_1</b> on a computer that doesn't have the Direct3D 11.1 runtime installed, this function immediately fails with E_INVALIDARG.
            </div>
<div> </div>

### -param FeatureLevels

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            The number of elements in <i>pFeatureLevels</i>.
          


### -param SDKVersion

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            The SDK version; use <i>D3D11_SDK_VERSION</i>.
          


### -param ppDevice [out, optional]

Type: <b><a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>**</b>


            Returns the address of a pointer to an <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> object that represents the device created. If this parameter is <b>NULL</b>, no ID3D11Device will be returned.
          


### -param pFeatureLevel [out, optional]

Type: <b><a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a>*</b>


            If successful, returns the first <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a> from the <i>pFeatureLevels</i> array which succeeded. Supply <b>NULL</b> as an input if you don't need to determine which feature level is supported.
          


### -param ppImmediateContext [out, optional]

Type: <b><a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>**</b>


            Returns the address of a pointer to an <a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a> object that represents the device context. If this parameter is <b>NULL</b>, no ID3D11DeviceContext will be returned.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method can return one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          


            This method returns E_INVALIDARG if you set the <i>pAdapter</i> parameter to a non-<b>NULL</b> value and the <i>DriverType</i> parameter to the D3D_DRIVER_TYPE_HARDWARE value.
          


            This method returns <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_SDK_COMPONENT_MISSING</a> if you specify <a href="d3d11_create_device_flag.htm">D3D11_CREATE_DEVICE_DEBUG</a> in <i>Flags</i> and the incorrect version of the <a href="overviews_direct3d_11_devices_layers.htm">debug layer</a> is installed on your computer. Install the latest Windows SDK to get the correct version.
          




## -remarks




          This entry-point is supported by the Direct3D 11 runtime, which is available on Windows 7, Windows Server 2008 R2, and as an update to
          Windows Vista (KB971644).
        


          To create a Direct3D 11.1 device (<a href="https://msdn.microsoft.com/DB4DAD13-3CD7-4362-950B-6403328CB071">ID3D11Device1</a>), which is available on Windows 8, Windows Server 2012, and Windows 7 and Windows Server 2008 R2 with the <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a> installed, you first create a <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> with this function, and then call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method on the <b>ID3D11Device</b> object to obtain the <b>ID3D11Device1</b> interface.
        


          To create a Direct3D 11.2 device (<a href="https://msdn.microsoft.com/C476AA0E-4A49-4E1E-8308-FB72EAD3E30C">ID3D11Device2</a>), which is available on Windows 8.1 and Windows Server 2012 R2, you first create a <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> with this function, and then call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method on the <b>ID3D11Device</b> object to obtain the <b>ID3D11Device2</b> interface.
        


          Set <i>ppDevice</i> and <i>ppImmediateContext</i> to <b>NULL</b> to determine which feature level is supported by looking
          at <i>pFeatureLevel</i> without creating a device.
        


          For an example, see <a href="https://msdn.microsoft.com/02a20ada-b3aa-435e-8d66-117a19222f9f">How To: Create a Device and Immediate Context</a>; to create a device and a swap chain at the same time,
          use <a href="https://msdn.microsoft.com/84d73e8c-f13c-4343-91de-57f9f8a0ad96">D3D11CreateDeviceAndSwapChain</a>.
        


          If you set the <i>pAdapter</i> parameter to a non-<b>NULL</b> value, you must also set the <i>DriverType</i> parameter to the D3D_DRIVER_TYPE_UNKNOWN value. If you set the <i>pAdapter</i> parameter to a non-<b>NULL</b> value and the <i>DriverType</i> parameter to the D3D_DRIVER_TYPE_HARDWARE value, <b>D3D11CreateDevice</b> returns an <a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a> of E_INVALIDARG.
        

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
<li>
                  If <i>DriverType</i> == D3D_DRIVER_TYPE_SOFTWARE,  <i>Software</i> cannot be <b>NULL</b>.
                </li>
<li>
                  If <i>DriverType</i> == D3D_DRIVER_TYPE_HARDWARE, the adapter used will be the default adapter, which is the first adapter that is enumerated by <a href="https://msdn.microsoft.com/23e876c7-b32a-4bc9-84c1-9e8949680e14">IDXGIFactory1::EnumAdapters</a>
</li>
</ul>
</td>
</tr>
</table>
 


        The function signature PFN_D3D11_CREATE_DEVICE is provided as a typedef, so that you can use dynamic linking techniques (<a href="https://msdn.microsoft.com/library/windows/desktop/ms683212(v=vs.85).aspx">GetProcAddress</a>) instead of statically linking.
      

<b>Windows Phone 8:
        </b> This API is supported.
      

<b>Windows Phone 8.1:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/3acbd433-c28d-4630-aa0e-25f2fb5c32d0">Core Functions</a>
 

 

