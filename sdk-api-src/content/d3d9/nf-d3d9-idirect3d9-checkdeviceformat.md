---
UID: NF:d3d9.IDirect3D9.CheckDeviceFormat
title: IDirect3D9::CheckDeviceFormat
author: windows-sdk-content
description: Determines whether a surface format is available as a specified resource type and can be used as a texture, depth-stencil buffer, or render target, or any combination of the three, on a device representing this adapter.
old-location: direct3d9\idirect3d9__checkdeviceformat.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__checkdeviceformat.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CheckDeviceFormat, CheckDeviceFormat method [Direct3D 9], CheckDeviceFormat method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],CheckDeviceFormat method, IDirect3D9.CheckDeviceFormat, IDirect3D9::CheckDeviceFormat, d3d9helper/IDirect3D9::CheckDeviceFormat, daa5cafd-0b8b-a747-98fe-eb9db7acde6d, direct3d9.idirect3d9__checkdeviceformat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3D9.CheckDeviceFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3D9::CheckDeviceFormat


## -description


Determines whether a surface format is available as a specified resource type and can be used as a texture, depth-stencil buffer, or render target, or any combination of the three, on a device representing this adapter.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number denoting the display adapter to query. <a href="https://msdn.microsoft.com/76f91917-394a-4588-9c83-c35bddb36b8e">D3DADAPTER_DEFAULT</a> is always the primary display adapter. This method returns D3DERR_INVALIDCALL when this value equals or exceeds the number of display adapters in the system. 


### -param DeviceType [in]

Type: <b><a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a> enumerated type, identifying the device type.


### -param AdapterFormat [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type, identifying the format of the display mode into which the adapter will be placed.


### -param Usage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Requested usage options for the surface. Usage options are any combination of <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a> and <a href="https://msdn.microsoft.com/d2030002-bd44-443f-8235-978919ebbda6">D3DUSAGE_QUERY</a> constants (only a subset of the D3DUSAGE constants are valid for <b>CheckDeviceFormat</b>; see the table on the D3DUSAGE page).


### -param RType [in]

Type: <b><a href="https://msdn.microsoft.com/6b360fb1-4a5a-47a2-bef9-d8234770bf0c">D3DRESOURCETYPE</a></b>

Resource type requested for use with the queried format. Member of <a href="https://msdn.microsoft.com/6b360fb1-4a5a-47a2-bef9-d8234770bf0c">D3DRESOURCETYPE</a>. 


### -param CheckFormat [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Format of the surfaces which may be used, as defined by Usage. Member of <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the format is compatible with the specified device for the requested usage, this method returns D3D_OK.

D3DERR_INVALIDCALL is returned if Adapter equals or exceeds the number of display adapters in the system, or if DeviceType is unsupported.

D3DERR_NOTAVAILABLE is returned if the format is not acceptable to the device for this usage.




## -remarks



Here are some examples using <b>CheckDeviceFormat</b> to check for hardware support of:

<ul>
<li>An off-screen plain surface format - Specify Usage = 0 and RType = D3DRTYPE_SURFACE.</li>
<li>A depth-stencil format - The following snippet tests for the passed in depth-stencil format:
    
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
BOOL IsDepthFormatExisting( D3DFORMAT DepthFormat, D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D-&gt;CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          D3DUSAGE_DEPTHSTENCIL,
                                          D3DRTYPE_SURFACE,
                                          DepthFormat);
    
    return SUCCEEDED( hr );
}</pre>
</td>
</tr>
</table></span></div>
See <a href="https://msdn.microsoft.com/d140b90c-3a20-49f4-883b-662b6c05dcea">Selecting a Device (Direct3D 9)</a> for more detail on the enumeration process.

</li>
<li>Can this texture be rendered in a particular format - Given the current display mode, this example shows how to verify that the texture format is compatible with the specific back-buffer format:
    
    
    
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
BOOL IsTextureFormatOk( D3DFORMAT TextureFormat, D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D-&gt;CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);
    
    return SUCCEEDED( hr );
}</pre>
</td>
</tr>
</table></span></div>
</li>
<li>Alpha blending in a pixel shader - Set Usage to <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE_QUERY_POSTPIXELSHADER_BLENDING</a>. Expect this to fail for all floating-point render targets.</li>
<li>Autogeneration of mipmaps - Set Usage to <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE_AUTOGENMIPMAP</a>. If the mipmap automatic generation fails, the application will get a non-mipmapped texture. Calling this method is considered a hint, so this method can return D3DOK_NOAUTOGEN (a valid success code) if the only thing that fails is the mipmap generation. For more information about mipmap generation, see <a href="https://msdn.microsoft.com/ae5955f9-e52a-41d7-a199-800e37a3e936">Automatic Generation of Mipmaps (Direct3D 9)</a>.</li>
</ul>
When migrating code from Direct3D 9 to Direct3D 10, the Direct3D 10 equivalent to CheckDeviceFormat is <a href="https://msdn.microsoft.com/50b4fcbb-3c51-4027-b766-ea0590eb7766">CheckFormatSupport</a>.




## -see-also




<a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>
 

 

