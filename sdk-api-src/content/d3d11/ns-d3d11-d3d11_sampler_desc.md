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

# D3D11_SAMPLER_DESC structure


## -description


Describes a sampler state.


## -struct-fields




### -field Filter

Type: <b><a href="https://msdn.microsoft.com/873b7910-4686-4f0c-a674-2aa3585a9b36">D3D11_FILTER</a></b>


            Filtering method to use when sampling a texture (see <a href="https://msdn.microsoft.com/873b7910-4686-4f0c-a674-2aa3585a9b36">D3D11_FILTER</a>).
          


### -field AddressU

Type: <b><a href="https://msdn.microsoft.com/4877e5db-011a-4a15-a087-5a55f229fa2a">D3D11_TEXTURE_ADDRESS_MODE</a></b>


            Method to use for resolving a u texture coordinate that is outside the 0 to 1 range (see <a href="https://msdn.microsoft.com/4877e5db-011a-4a15-a087-5a55f229fa2a">D3D11_TEXTURE_ADDRESS_MODE</a>).
          


### -field AddressV

Type: <b><a href="https://msdn.microsoft.com/4877e5db-011a-4a15-a087-5a55f229fa2a">D3D11_TEXTURE_ADDRESS_MODE</a></b>

Method to use for resolving a v texture coordinate that is outside the 0 to 1 range.


### -field AddressW

Type: <b><a href="https://msdn.microsoft.com/4877e5db-011a-4a15-a087-5a55f229fa2a">D3D11_TEXTURE_ADDRESS_MODE</a></b>

Method to use for resolving a w texture coordinate that is outside the 0 to 1 range.


### -field MipLODBias

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Offset from the calculated mipmap level. For example, if Direct3D calculates that a texture should be sampled at mipmap level 3 and MipLODBias is 2, then the texture will be sampled at mipmap level 5.


### -field MaxAnisotropy

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Clamping value used if D3D11_FILTER_ANISOTROPIC or D3D11_FILTER_COMPARISON_ANISOTROPIC is specified in Filter. Valid values are between 1 and 16.


### -field ComparisonFunc

Type: <b><a href="https://msdn.microsoft.com/3546c7b8-ae25-4554-85e2-527433a74a94">D3D11_COMPARISON_FUNC</a></b>


            A function that compares sampled data against existing sampled data. The function options are listed in <a href="https://msdn.microsoft.com/3546c7b8-ae25-4554-85e2-527433a74a94">D3D11_COMPARISON_FUNC</a>.
          


### -field BorderColor

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a>[4]</b>

Border color to use if D3D11_TEXTURE_ADDRESS_BORDER is specified for AddressU, AddressV, or AddressW. Range must be between 0.0 and 1.0 inclusive.


### -field MinLOD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Lower end of the mipmap range to clamp access to, where 0 is the largest and most detailed mipmap level and any level higher than that is less detailed.


### -field MaxLOD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Upper end of the mipmap range to clamp access to, where 0 is the largest and most detailed mipmap level and any level higher than that is less detailed. This value must be greater than or equal to MinLOD. To have no upper limit on LOD set this to a large value such as D3D11_FLOAT32_MAX.


## -remarks



These are the default values for sampler state.

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td>Filter</td>
<td>D3D11_FILTER_MIN_MAG_MIP_LINEAR</td>
</tr>
<tr>
<td>AddressU</td>
<td>D3D11_TEXTURE_ADDRESS_CLAMP</td>
</tr>
<tr>
<td>AddressV</td>
<td>D3D11_TEXTURE_ADDRESS_CLAMP</td>
</tr>
<tr>
<td>AddressW</td>
<td>D3D11_TEXTURE_ADDRESS_CLAMP</td>
</tr>
<tr>
<td>MinLOD</td>
<td>-3.402823466e+38F (-FLT_MAX)</td>
</tr>
<tr>
<td>MaxLOD</td>
<td>3.402823466e+38F (FLT_MAX)</td>
</tr>
<tr>
<td>MipMapLODBias</td>
<td>0.0f</td>
</tr>
<tr>
<td>MaxAnisotropy</td>
<td>1</td>
</tr>
<tr>
<td>ComparisonFunc</td>
<td>D3D11_COMPARISON_NEVER</td>
</tr>
<tr>
<td>BorderColor</td>
<td>float4(1.0f,1.0f,1.0f,1.0f)</td>
</tr>
<tr>
<td>Texture</td>
<td>N/A</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>
 

 

