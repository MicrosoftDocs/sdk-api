---
UID: NS:d3d11.D3D11_FEATURE_DATA_D3D9_OPTIONS1
title: D3D11_FEATURE_DATA_D3D9_OPTIONS1
author: windows-sdk-content
description: Describes Direct3D 9 feature options in the current graphics driver.
old-location: direct3d11\d3d11_feature_data_d3d9_options1.htm
tech.root: direct3d11
ms.assetid: 4894B4FC-1E95-42B1-B92D-E3B484ABDC74
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_FEATURE_DATA_D3D9_OPTIONS1, D3D11_FEATURE_DATA_D3D9_OPTIONS1 structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_D3D9_OPTIONS1, direct3d11.d3d11_feature_data_d3d9_options1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_FEATURE_DATA_D3D9_OPTIONS1
product: Windows
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_D3D9_OPTIONS1
req.redist: 
---

# D3D11_FEATURE_DATA_D3D9_OPTIONS1 structure


## -description


<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.2 runtime, which is available on Windows 8.1 and later operating systems.</div><div> </div>Describes Direct3D 9 feature options in the current graphics driver.


## -struct-fields




### -field FullNonPow2TextureSupported

Specifies whether the driver supports the nonpowers-of-2-unconditionally feature. For more info about this feature, see <a href="https://msdn.microsoft.com/en-us/library/Ff476876(v=VS.85).aspx">feature level</a>. The runtime sets this member to <b>TRUE</b> for hardware at Direct3D 10 and higher feature levels.  For hardware at Direct3D 9.3 and lower feature levels, the runtime sets this member to <b>FALSE</b> if the hardware and driver support the powers-of-2 (2D textures must have widths and heights specified as powers of two) feature or the nonpowers-of-2-conditionally feature. 


### -field DepthAsTextureWithLessEqualComparisonFilterSupported

Specifies whether the driver supports the shadowing feature with the comparison-filtering mode set to less than or equal to. The runtime sets this member to <b>TRUE</b> for hardware at Direct3D 10 and higher <a href="https://msdn.microsoft.com/en-us/library/Ff476876(v=VS.85).aspx">feature levels</a>.  For hardware at Direct3D 9.3 and lower feature levels, the runtime sets this member to <b>TRUE</b> only if the hardware and driver support the shadowing feature; otherwise <b>FALSE</b>. 


### -field SimpleInstancingSupported

Specifies whether the hardware and driver support simple instancing. The runtime sets this member to <b>TRUE</b> if  the hardware and driver support simple instancing.


### -field TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported

Specifies whether the hardware and driver support setting a single face of a <a href="https://msdn.microsoft.com/en-us/library/Dn367022(v=VS.85).aspx">TextureCube</a> as a render target while the depth stencil surface that is bound alongside can be a <a href="https://msdn.microsoft.com/en-us/library/Ff471525(v=VS.85).aspx">Texture2D</a> (as opposed to <b>TextureCube</b>). The runtime sets this member to <b>TRUE</b> if  the hardware and driver support this feature; otherwise <b>FALSE</b>.

If the hardware and driver don't support this feature, the app must match the render target surface type with the depth stencil surface type. Because hardware at Direct3D 9.3 and lower <a href="https://msdn.microsoft.com/en-us/library/Ff476876(v=VS.85).aspx">feature levels</a> doesn't allow <a href="https://msdn.microsoft.com/en-us/library/Dn367022(v=VS.85).aspx">TextureCube</a> depth surfaces, the only way to render a scene into a <b>TextureCube</b> while having depth buffering enabled is to render each <b>TextureCube</b> face separately to a <a href="https://msdn.microsoft.com/en-us/library/Ff471525(v=VS.85).aspx">Texture2D</a> render target first (because that can be matched with a <b>Texture2D</b> depth), and then copy the results into the <b>TextureCube</b>.  If  the hardware and driver support this feature, the app can just render to the <b>TextureCube</b> faces directly while getting depth buffering out of a <b>Texture2D</b> depth buffer.

You only need to query this feature from  hardware at Direct3D 9.3 and lower <a href="https://msdn.microsoft.com/en-us/library/Ff476876(v=VS.85).aspx">feature levels</a> because hardware at Direct3D 10.0 and higher feature levels allow <a href="https://msdn.microsoft.com/en-us/library/Dn367022(v=VS.85).aspx">TextureCube</a> depth surfaces.


## -remarks



You can use the <a href="https://msdn.microsoft.com/en-us/library/Ff476124(v=VS.85).aspx">D3D11_FEATURE_D3D9_OPTIONS1</a> enumeration value with <a href="https://msdn.microsoft.com/en-us/library/Ff476497(v=VS.85).aspx">ID3D11Device::CheckFeatureSupport</a> to query a driver about support for Direct3D 9 feature options rather than making multiple calls to <b>ID3D11Device::CheckFeatureSupport</b> by using <a href="https://msdn.microsoft.com/en-us/library/Ff476124(v=VS.85).aspx">D3D11_FEATURE_D3D9_OPTIONS</a>, <b>D3D11_FEATURE_D3D9_SHADOW_SUPPORT</b>, and <b>D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT</b>, which provide identical info about supported Direct3D 9 feature options.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476124(v=VS.85).aspx">D3D11_FEATURE</a>
 

 

