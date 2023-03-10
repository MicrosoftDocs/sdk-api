---
UID: NS:d3d11.D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT
title: D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT (d3d11.h)
description: Describes Direct3D 9 shadow support in the current graphics driver.
helpviewer_keywords: ["D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT","D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT structure [Direct3D 11]","d3d11/D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT","direct3d11.d3d11_feature_data_d3d9_shadow_support"]
old-location: direct3d11\d3d11_feature_data_d3d9_shadow_support.htm
tech.root: direct3d11
ms.assetid: E30500A0-D77D-4783-A5D5-418770DA1376
ms.date: 12/05/2018
ms.keywords: D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT, D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT, direct3d11.d3d11_feature_data_d3d9_shadow_support
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT
 - d3d11/D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT
---

# D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT structure


## -description

<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</div><div> </div>Describes Direct3D 9 shadow support in the current graphics driver.

## -struct-fields

### -field SupportsDepthAsTextureWithLessEqualComparisonFilter

Specifies whether the driver supports the shadowing feature with the comparison-filtering mode set to less than or equal to. The runtime sets this member to <b>TRUE</b> for hardware at Direct3D 10 and higher <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature levels</a>.  For hardware at Direct3D 9.3 and lower feature levels, the runtime sets this member to <b>TRUE</b> only if the hardware and driver support the shadowing feature; otherwise <b>FALSE</b>.

## -remarks

Shadows are an important element in realistic 3D scenes.  You can use the shadow buffer technique to render shadows.  The basic principle of the technique is to use a depth buffer to store the scene depth info from the perspective of the light source, and then compare each point rendered in the scene with that buffer to determine if it is in shadow.

To render objects into the scene with shadows on them, you create <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler">sampler state objects</a> with comparison filtering set and  the comparison mode (ComparisonFunc) to LessEqual.  You can also set BorderColor addressing on this depth sampler, even though BorderColor isn't typically allowed on <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature levels</a> 9.1 and 9.2.  By using the border color and picking 0.0 or 1.0 as the border color value, you can control whether the regions off the edge of the shadow map appear to be always in shadow or never in shadow respectively.
You can control the shadow filter quality by the Mag and Min filter settings in the comparison sampler.  Point sampling will produce shadows with non-anti-aliased edges.  Linear filter sampler settings will result in higher quality shadow edges, but might affect performance on some power-optimized devices.

<div class="alert"><b>Note</b>  If you use a separate setting for Mag versus Min filter options, you produce an undefined result.  Anisotropic filtering is not supported. The Mip filter choice is not relevant because <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9.x does not allow mipmapped depth buffers.</div>
<div> </div>
<div class="alert"><b>Note</b>  On <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 9.x, you can't compile a shader with the <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmp">SampleCmp</a> and <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-samplecmplevelzero">SampleCmpLevelZero</a> intrinsic functions by using older versions of the compiler. For example,  you can't use the <a href="/windows/desktop/direct3dtools/fxc">fxc.exe</a> compiler that ships with the DirectX SDK or use the <b>D3DCompile**</b> functions (like <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile">D3DCompileFromFile</a>) that are implemented in D3DCompiler_43.dll and earlier. These intrinsic functions on feature level 9.x are only supported in the fxc.exe compiler that ships with the Windows 8 SDK and later and with the <b>D3DCompile**</b> functions that are implemented in D3DCompiler_44.dll and later.
But these intrinsic functions are present in shader models for feature levels higher than 9.x.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE</a>