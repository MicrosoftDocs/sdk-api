---
UID: NF:d3d9helper.IDirect3D9.CheckDeviceFormatConversion
title: IDirect3D9::CheckDeviceFormatConversion
author: windows-sdk-content
description: Tests the device to see if it supports conversion from one display format to another.
old-location: direct3d9\idirect3d9__checkdeviceformatconversion.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__checkdeviceformatconversion.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CheckDeviceFormatConversion, CheckDeviceFormatConversion method [Direct3D 9], CheckDeviceFormatConversion method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],CheckDeviceFormatConversion method, IDirect3D9.CheckDeviceFormatConversion, IDirect3D9::CheckDeviceFormatConversion, a6fe9dd6-8eae-cbfc-8047-efc7175e6688, d3d9helper/IDirect3D9::CheckDeviceFormatConversion, direct3d9.idirect3d9__checkdeviceformatconversion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9helper.h
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
 - IDirect3D9.CheckDeviceFormatConversion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d9helper.h
: 
- IDirect3D9.CheckDeviceFormatConversion
: 
---

# IDirect3D9::CheckDeviceFormatConversion


## -description


Tests the device to see if it supports conversion from one display format to another.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Display adapter ordinal number. D3DADAPTER_DEFAULT is always the primary display adapter. This method returns D3DERR_INVALIDCALL when this value equals or exceeds the number of display adapters in the system. 


### -param DeviceType [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172547(v=VS.85).aspx">D3DDEVTYPE</a></b>

Device type. Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172547(v=VS.85).aspx">D3DDEVTYPE</a> enumerated type. 


### -param SourceFormat [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a></b>

Source adapter format. Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a> enumerated type.


### -param TargetFormat [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a></b>

Target adapter format. Member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a> enumerated type.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value is D3DERR_INVALIDCALL.
 The method will return D3DERR_NOTAVAILABLE when the hardware does not support conversion between the two formats.




## -remarks



Using <a href="https://msdn.microsoft.com/en-us/library/Bb174312(v=VS.85).aspx">CheckDeviceType</a> to test for compatibility between a back buffer that differs from the display format will return appropriate values. This means that the call will reflect device capabilities. If the device cannot render to the requested back buffer format, the call will still return D3DERR_NOTAVAILABLE. If the device can render to the format, but cannot perform the color-converting presentation, the return value will also be D3DERR_NOTAVAILABLE. Applications can discover hardware support for the presentation itself by calling <b>CheckDeviceFormatConversion</b>. No software emulation for the color-converting presentation itself will be offered.

<b>CheckDeviceFormatConversion</b> can also be used to determine which combinations of source surface formats and destination surface formats are permissible in calls to <a href="https://msdn.microsoft.com/en-us/library/Bb174471(v=VS.85).aspx">StretchRect</a>.
    


Color conversion is restricted to the following source and target formats.

<ul>
<li>The source format must be a FOURCC format or a valid back buffer format. For a list of these, see <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">FourCC Formats</a> and BackBuffer or Display Formats.</li>
<li>The target format must be one of these unsigned formats:
    
    
    
<table>
<tr>
<td>D3DFMT_X1R5G5B5</td>
<td>D3DFMT_A1R5G5B5</td>
<td>D3DFMT_R5G6B5</td>
</tr>
<tr>
<td>D3DFMT_R8G8B8</td>
<td>D3DFMT_X8R8G8B8</td>
<td>D3DFMT_A8R8G8B8</td>
</tr>
<tr>
<td>D3DFMT_A2R10G10B10</td>
<td>D3DFMT_A16B16G16R16</td>
<td>D3DFMT_A2B10G10R10</td>
</tr>
<tr>
<td>D3DFMT_A8B8G8R8</td>
<td>D3DFMT_X8B8G8R8</td>
<td>D3DFMT_A16B16G16R16F</td>
</tr>
<tr>
<td>D3DFMT_A32B32G32R32F</td>
<td></td>
<td></td>
</tr>
</table>
 

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174353(v=VS.85).aspx">ColorFill</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174300(v=VS.85).aspx">IDirect3D9</a>
 

 

