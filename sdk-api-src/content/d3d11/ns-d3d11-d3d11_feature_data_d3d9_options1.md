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

# D3D11_FEATURE_DATA_D3D9_OPTIONS1 structure


## -description


<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.2 runtime, which is available on Windows 8.1 and later operating systems.</div><div> </div>Describes Direct3D 9 feature options in the current graphics driver.


## -struct-fields




### -field FullNonPow2TextureSupported

Specifies whether the driver supports the nonpowers-of-2-unconditionally feature. For more info about this feature, see <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a>. The runtime sets this member to <b>TRUE</b> for hardware at Direct3D 10 and higher feature levels.  For hardware at Direct3D 9.3 and lower feature levels, the runtime sets this member to <b>FALSE</b> if the hardware and driver support the powers-of-2 (2D textures must have widths and heights specified as powers of two) feature or the nonpowers-of-2-conditionally feature. 


### -field DepthAsTextureWithLessEqualComparisonFilterSupported

Specifies whether the driver supports the shadowing feature with the comparison-filtering mode set to less than or equal to. The runtime sets this member to <b>TRUE</b> for hardware at Direct3D 10 and higher <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature levels</a>.  For hardware at Direct3D 9.3 and lower feature levels, the runtime sets this member to <b>TRUE</b> only if the hardware and driver support the shadowing feature; otherwise <b>FALSE</b>. 


### -field SimpleInstancingSupported

Specifies whether the hardware and driver support simple instancing. The runtime sets this member to <b>TRUE</b> if  the hardware and driver support simple instancing.


### -field TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported

Specifies whether the hardware and driver support setting a single face of a <a href="https://msdn.microsoft.com/BC96D7BB-992E-48CC-A774-E211E1BB1720">TextureCube</a> as a render target while the depth stencil surface that is bound alongside can be a <a href="https://msdn.microsoft.com/e4f9cfd8-65e6-4375-8f87-736bca32cad4">Texture2D</a> (as opposed to <b>TextureCube</b>). The runtime sets this member to <b>TRUE</b> if  the hardware and driver support this feature; otherwise <b>FALSE</b>.

If the hardware and driver don't support this feature, the app must match the render target surface type with the depth stencil surface type. Because hardware at Direct3D 9.3 and lower <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature levels</a> doesn't allow <a href="https://msdn.microsoft.com/BC96D7BB-992E-48CC-A774-E211E1BB1720">TextureCube</a> depth surfaces, the only way to render a scene into a <b>TextureCube</b> while having depth buffering enabled is to render each <b>TextureCube</b> face separately to a <a href="https://msdn.microsoft.com/e4f9cfd8-65e6-4375-8f87-736bca32cad4">Texture2D</a> render target first (because that can be matched with a <b>Texture2D</b> depth), and then copy the results into the <b>TextureCube</b>.  If  the hardware and driver support this feature, the app can just render to the <b>TextureCube</b> faces directly while getting depth buffering out of a <b>Texture2D</b> depth buffer.

You only need to query this feature from  hardware at Direct3D 9.3 and lower <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature levels</a> because hardware at Direct3D 10.0 and higher feature levels allow <a href="https://msdn.microsoft.com/BC96D7BB-992E-48CC-A774-E211E1BB1720">TextureCube</a> depth surfaces.


## -remarks



You can use the <a href="d3d11_feature.htm">D3D11_FEATURE_D3D9_OPTIONS1</a> enumeration value with <a href="https://msdn.microsoft.com/7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1">ID3D11Device::CheckFeatureSupport</a> to query a driver about support for Direct3D 9 feature options rather than making multiple calls to <b>ID3D11Device::CheckFeatureSupport</b> by using <a href="d3d11_feature.htm">D3D11_FEATURE_D3D9_OPTIONS</a>, <b>D3D11_FEATURE_D3D9_SHADOW_SUPPORT</b>, and <b>D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT</b>, which provide identical info about supported Direct3D 9 feature options.




## -see-also




<a href="https://msdn.microsoft.com/2a45182a-7114-4075-b8b8-147f52fe7aa9">Core Structures</a>



<a href="https://msdn.microsoft.com/48c3bf65-f077-45e6-a306-03d5760eeccb">D3D11_FEATURE</a>
 

 

