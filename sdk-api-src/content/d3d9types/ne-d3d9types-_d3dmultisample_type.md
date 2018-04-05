---
UID: NE:d3d9types._D3DMULTISAMPLE_TYPE
title: "_D3DMULTISAMPLE_TYPE"
author: windows-driver-content
description: Defines the levels of full-scene multisampling that the device can apply.
old-location: direct3d9\D3DMULTISAMPLE_TYPE.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dmultisample_type.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 65f8f87f-09f6-ee7e-9319-94419df35aca, D3DMULTISAMPLE_10_SAMPLES, D3DMULTISAMPLE_11_SAMPLES, D3DMULTISAMPLE_12_SAMPLES, D3DMULTISAMPLE_13_SAMPLES, D3DMULTISAMPLE_14_SAMPLES, D3DMULTISAMPLE_15_SAMPLES, D3DMULTISAMPLE_16_SAMPLES, D3DMULTISAMPLE_2_SAMPLES, D3DMULTISAMPLE_3_SAMPLES, D3DMULTISAMPLE_4_SAMPLES, D3DMULTISAMPLE_5_SAMPLES, D3DMULTISAMPLE_6_SAMPLES, D3DMULTISAMPLE_7_SAMPLES, D3DMULTISAMPLE_8_SAMPLES, D3DMULTISAMPLE_9_SAMPLES, D3DMULTISAMPLE_FORCE_DWORD, D3DMULTISAMPLE_NONE, D3DMULTISAMPLE_NONMASKABLE, D3DMULTISAMPLE_TYPE, D3DMULTISAMPLE_TYPE enumeration [Direct3D 9], LPD3DMULTISAMPLE_TYPE, LPD3DMULTISAMPLE_TYPE enumeration pointer [Direct3D 9], _D3DMULTISAMPLE_TYPE, d3d9types/D3DMULTISAMPLE_10_SAMPLES, d3d9types/D3DMULTISAMPLE_11_SAMPLES, d3d9types/D3DMULTISAMPLE_12_SAMPLES, d3d9types/D3DMULTISAMPLE_13_SAMPLES, d3d9types/D3DMULTISAMPLE_14_SAMPLES, d3d9types/D3DMULTISAMPLE_15_SAMPLES, d3d9types/D3DMULTISAMPLE_16_SAMPLES, d3d9types/D3DMULTISAMPLE_2_SAMPLES, d3d9types/D3DMULTISAMPLE_3_SAMPLES, d3d9types/D3DMULTISAMPLE_4_SAMPLES, d3d9types/D3DMULTISAMPLE_5_SAMPLES, d3d9types/D3DMULTISAMPLE_6_SAMPLES, d3d9types/D3DMULTISAMPLE_7_SAMPLES, d3d9types/D3DMULTISAMPLE_8_SAMPLES, d3d9types/D3DMULTISAMPLE_9_SAMPLES, d3d9types/D3DMULTISAMPLE_FORCE_DWORD, d3d9types/D3DMULTISAMPLE_NONE, d3d9types/D3DMULTISAMPLE_NONMASKABLE, d3d9types/D3DMULTISAMPLE_TYPE, d3d9types/LPD3DMULTISAMPLE_TYPE, direct3d9.D3DMULTISAMPLE_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d9types.h
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
req.typenames: D3DMULTISAMPLE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DMULTISAMPLE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DMULTISAMPLE_TYPE enumeration


## -description


Defines the levels of full-scene multisampling that the device can apply.


## -enum-fields




### -field D3DMULTISAMPLE_NONE

No level of full-scene multisampling is available. 


### -field D3DMULTISAMPLE_NONMASKABLE

Enables the multisample quality value. See Remarks. 


### -field D3DMULTISAMPLE_2_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_3_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_4_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_5_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_6_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_7_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_8_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_9_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_10_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_11_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_12_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_13_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_14_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_15_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_16_SAMPLES

Level of full-scene multisampling available. 


### -field D3DMULTISAMPLE_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



In addition to enabling full-scene multisampling at <a href="https://msdn.microsoft.com/6d672f22-9843-4ff7-ae79-4903f56cd1e9">IDirect3DDevice9::Reset</a> time, there will be render states that turn various aspects on and off at fine-grained levels.

Multisampling is valid only on a swap chain that is being created or reset with the D3DSWAPEFFECT_DISCARD swap effect.

The multisample antialiasing value can be set with the parameters (or sub-parameters) in the following methods.

<table>
<tr>
<th>Method</th>
<th>Parameters</th>
<th>Sub-parameters</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/82f1f1f6-0d9b-497b-b532-0d2aabbd0314">IDirect3D9::CheckDeviceMultiSampleType</a>
</td>
<td>MultiSampleType and pQualityLevels</td>
<td></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">IDirect3D9::CreateDevice</a>
</td>
<td>pPresentationParameters</td>
<td>MultiSampleType and pQualityLevels</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/d41b36f6-8481-47f8-bd38-8f51bc9ff9b8">IDirect3DDevice9::CreateAdditionalSwapChain</a>
</td>
<td>pPresentationParameters</td>
<td>MultiSampleType and pQualityLevels</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c94eed81-0706-44d6-a8be-83e2a5d46c39">IDirect3DDevice9::CreateDepthStencilSurface</a>
</td>
<td>MultiSampleType and pQualityLevels</td>
<td></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3c0c8651-0c54-4eeb-bd37-c2aa26b1211d">IDirect3DDevice9::CreateRenderTarget</a>
</td>
<td>MultiSampleType and pQualityLevels</td>
<td></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6d672f22-9843-4ff7-ae79-4903f56cd1e9">IDirect3DDevice9::Reset</a>
</td>
<td>pPresentationParameters</td>
<td>MultiSampleType and pQualityLevels</td>
</tr>
</table>
 

It is not good practice to switch from one multisample type to another to raise the quality of the antialiasing.

D3DMULTISAMPLE_NONE enables swap effects other than discarding, locking, and so on.

Whether the display device supports maskable multisampling (more than one sample for a multiple-sample render-target format plus antialias support) or just non-maskable multisampling (only antialias support), the driver for the device provides the number of quality levels for the D3DMULTISAMPLE_NONMASKABLE multiple-sample type. Applications that just use multisampling for antialiasing purposes only need to query for the number of non-maskable multiple-sample quality levels that the driver supports.

The quality levels supported by the device can be obtained with the pQualityLevels parameter of <a href="https://msdn.microsoft.com/82f1f1f6-0d9b-497b-b532-0d2aabbd0314">IDirect3D9::CheckDeviceMultiSampleType</a>. Quality levels used by the application are set with the MultiSampleQuality parameter of <a href="https://msdn.microsoft.com/c94eed81-0706-44d6-a8be-83e2a5d46c39">IDirect3DDevice9::CreateDepthStencilSurface</a> and <a href="https://msdn.microsoft.com/3c0c8651-0c54-4eeb-bd37-c2aa26b1211d">IDirect3DDevice9::CreateRenderTarget</a>.

See D3DRS_MULTISAMPLEMASK for discussion of maskable multisampling.




## -see-also




<a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a>



<a href="https://msdn.microsoft.com/fad8ffdb-36e5-4695-b343-e1315357c31a">D3DSURFACE_DESC</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

