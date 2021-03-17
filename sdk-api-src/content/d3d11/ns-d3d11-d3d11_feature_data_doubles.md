---
UID: NS:d3d11.D3D11_FEATURE_DATA_DOUBLES
title: D3D11_FEATURE_DATA_DOUBLES (d3d11.h)
description: Describes double data type support in the current graphics driver.
helpviewer_keywords: ["D3D11_FEATURE_DATA_DOUBLES","D3D11_FEATURE_DATA_DOUBLES structure [Direct3D 11]","d3d11/D3D11_FEATURE_DATA_DOUBLES","dde276ab-cd61-a449-9965-674c9221da9c","direct3d11.d3d11_feature_data_doubles"]
old-location: direct3d11\d3d11_feature_data_doubles.htm
tech.root: direct3d11
ms.assetid: 3cd4006b-25bd-46b8-9fa7-6b7d7eb82a75
ms.date: 12/05/2018
ms.keywords: D3D11_FEATURE_DATA_DOUBLES, D3D11_FEATURE_DATA_DOUBLES structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_DOUBLES, dde276ab-cd61-a449-9965-674c9221da9c, direct3d11.d3d11_feature_data_doubles
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_DOUBLES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE_DATA_DOUBLES
 - d3d11/D3D11_FEATURE_DATA_DOUBLES
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
 - D3D11_FEATURE_DATA_DOUBLES
---

# D3D11_FEATURE_DATA_DOUBLES structure


## -description

Describes double data type support in the current graphics driver.

## -struct-fields

### -field DoublePrecisionFloatShaderOps

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar">double</a> types are allowed. If <b>TRUE</b>, <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar">double</a> types are allowed; otherwise <b>FALSE</b>. The runtime must set <b>DoublePrecisionFloatShaderOps</b> to  <b>TRUE</b> in order for you to use any <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> shader that is compiled with a <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar">double</a> type.

## -remarks

If the runtime sets <b>DoublePrecisionFloatShaderOps</b> to  <b>TRUE</b>, the hardware and driver support the following <a href="/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5">Shader Model 5</a> instructions:

<ul>
<li>
<a href="/windows/desktop/direct3dhlsl/dadd---sm5---asm-">dadd</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/dmax--sm5---asm-">dmax</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/dmin--sm5---asm-">dmin</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/dmul--sm5---asm-">dmul</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/deq--sm5---asm-">deq</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/dge--sm5---asm-">dge</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/dlt--sm5---asm-">dlt</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/dne--sm5---asm-">dne</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/dmov--sm5---asm-">dmov</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/dmovc--sm5---asm-">dmovc</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/dtof--sm5---asm-">dtof</a>
</li>
<li>
<a href="/windows/desktop/direct3dhlsl/ftod--sm5---asm-">ftod</a>
</li>
</ul>
<div class="alert"><b>Note</b>  If <b>DoublePrecisionFloatShaderOps</b> is <b>TRUE</b>, the hardware and driver do not necessarily support double-precision division.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>