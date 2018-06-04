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

# IDirect3D9::CheckDeviceMultiSampleType


## -description


Determines if a multisampling technique is available on this device.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number denoting the display adapter to query. D3DADAPTER_DEFAULT is always the primary display adapter. This method returns <b>FALSE</b> when this value equals or exceeds the number of display adapters in the system. See Remarks.


### -param DeviceType [in]

Type: <b><a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/2bcdc476-7c42-4152-b107-58366faf2abd">D3DDEVTYPE</a> enumerated type, identifying the device type.


### -param SurfaceFormat [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type that specifies the format of the surface to be multisampled. For more information, see Remarks.


### -param Windowed [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

bool value. Specify <b>TRUE</b> to inquire about windowed multisampling, and specify <b>FALSE</b> to inquire about full-screen multisampling.


### -param MultiSampleType [in]

Type: <b><a href="https://msdn.microsoft.com/1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8">D3DMULTISAMPLE_TYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8">D3DMULTISAMPLE_TYPE</a> enumerated type, identifying the multisampling technique to test.


### -param pQualityLevels [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

<b>pQualityLevels</b> returns the number of device-specific sampling variations available with the given sample type. For example, if the returned value is 3, then quality levels 0, 1 and 2 can be used when creating resources with the given sample count. The meanings of these quality levels are defined by the device manufacturer and cannot be queried through D3D. For example, for a particular device different quality levels at a fixed sample count might refer to different spatial layouts of the sample locations or different methods of resolving.  This can be <b>NULL</b> if it is not necessary to return the quality levels.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the device can perform the specified multisampling method, this method returns D3D_OK.
 D3DERR_INVALIDCALL is returned if the Adapter or MultiSampleType parameters are invalid. This method returns D3DERR_NOTAVAILABLE if the queried multisampling technique is not supported by this device. D3DERR_INVALIDDEVICE is returned if DeviceType does not apply to this adapter.




## -remarks



This method is intended for use with both render-target and depth-stencil surfaces because you must create both surfaces multisampled if you want to use them together.

The following code fragment shows how you could use <b>CheckDeviceMultiSampleType</b> to test for devices that support a specific multisampling method.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
if( SUCCEEDED(pD3D-&gt;CheckDeviceMultiSampleType( pCaps-&gt;AdapterOrdinal, 
                                pCaps-&gt;DeviceType, BackBufferFormat, 
                                FALSE, D3DMULTISAMPLE_3_SAMPLES, NULL ) ) &amp;&amp;
         SUCCEEDED(pD3D-&gt;CheckDeviceMultiSampleType( pCaps-&gt;AdapterOrdinal, 
                                pCaps-&gt;DeviceType, DepthBufferFormat, 
                                FALSE, D3DMULTISAMPLE_3_SAMPLES, NULL ) ) )
    return S_OK;
</pre>
</td>
</tr>
</table></span></div>
The preceding code will return S_OK if the device supports the full-screen D3DMULTISAMPLE_3_SAMPLES multisampling method with the surface format.

See the remarks in <a href="https://msdn.microsoft.com/1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8">D3DMULTISAMPLE_TYPE</a> for additional information on working with and setting multisample types and quality levels.




## -see-also




<a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>
 

 

