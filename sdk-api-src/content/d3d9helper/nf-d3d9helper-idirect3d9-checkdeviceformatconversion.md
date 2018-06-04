---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirect3D9::CheckDeviceFormatConversion


## -description


Tests the device to see if it supports conversion from one display format to another.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Display adapter ordinal number. D3DADAPTER_DEFAULT is always the primary display adapter. This method returns D3DERR_INVALIDCALL when this value equals or exceeds the number of display adapters in the system. 


### -param DeviceType [in]

Type: <b><a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a></b>

Device type. Member of the <a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a> enumerated type. 


### -param SourceFormat [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Source adapter format. Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type.


### -param TargetFormat [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Target adapter format. Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value is D3DERR_INVALIDCALL.
 The method will return D3DERR_NOTAVAILABLE when the hardware does not support conversion between the two formats.




## -remarks



Using <a href="https://msdn.microsoft.com/bd19079c-d0ee-4e2f-8a02-9f26c8abcb31">CheckDeviceType</a> to test for compatibility between a back buffer that differs from the display format will return appropriate values. This means that the call will reflect device capabilities. If the device cannot render to the requested back buffer format, the call will still return D3DERR_NOTAVAILABLE. If the device can render to the format, but cannot perform the color-converting presentation, the return value will also be D3DERR_NOTAVAILABLE. Applications can discover hardware support for the presentation itself by calling <b>CheckDeviceFormatConversion</b>. No software emulation for the color-converting presentation itself will be offered.

<b>CheckDeviceFormatConversion</b> can also be used to determine which combinations of source surface formats and destination surface formats are permissible in calls to <a href="https://msdn.microsoft.com/1ad6d48f-8420-461a-96b5-e730ac06c393">StretchRect</a>.
    


Color conversion is restricted to the following source and target formats.

<ul>
<li>The source format must be a FOURCC format or a valid back buffer format. For a list of these, see <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">FourCC Formats</a> and BackBuffer or Display Formats.</li>
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




<a href="https://msdn.microsoft.com/de8c1f15-cb82-4c20-86e0-78b730dae55d">ColorFill</a>



<a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>
 

 

