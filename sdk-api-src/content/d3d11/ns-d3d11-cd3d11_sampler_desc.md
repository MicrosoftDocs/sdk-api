---
UID: NS:d3d11.CD3D11_SAMPLER_DESC
title: CD3D11_SAMPLER_DESC (d3d11.h)
description: Represents a sampler state and provides convenience methods for creating sampler states.
helpviewer_keywords: ["CD3D11_SAMPLER_DESC","CD3D11_SAMPLER_DESC structure [Direct3D 11]","d3d11/CD3D11_SAMPLER_DESC","direct3d11.cd3d11_sampler_desc"]
old-location: direct3d11\cd3d11_sampler_desc.htm
tech.root: direct3d11
ms.assetid: 1FE748DB-7DC6-4C6E-94D5-DF88477B3DEC
ms.date: 12/05/2018
ms.keywords: CD3D11_SAMPLER_DESC, CD3D11_SAMPLER_DESC structure [Direct3D 11], d3d11/CD3D11_SAMPLER_DESC, direct3d11.cd3d11_sampler_desc
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CD3D11_SAMPLER_DESC
 - d3d11/CD3D11_SAMPLER_DESC
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
 - CD3D11_SAMPLER_DESC
---

# CD3D11_SAMPLER_DESC structure


## -description

Represents a sampler state and provides convenience methods for creating sampler states.

## -struct-fields

## -remarks

Here is how D3D11.h defines <b>CD3D11_SAMPLER_DESC</b>:

<div class="code"><span><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
struct CD3D11_SAMPLER_DESC : public D3D11_SAMPLER_DESC
{
    CD3D11_SAMPLER_DESC()
    {}
    explicit CD3D11_SAMPLER_DESC( const D3D11_SAMPLER_DESC&amp; o ) :
        D3D11_SAMPLER_DESC( o )
    {}
    explicit CD3D11_SAMPLER_DESC( CD3D11_DEFAULT )
    {
        Filter = D3D11_FILTER_MIN_MAG_MIP_LINEAR;
        AddressU = D3D11_TEXTURE_ADDRESS_CLAMP;
        AddressV = D3D11_TEXTURE_ADDRESS_CLAMP;
        AddressW = D3D11_TEXTURE_ADDRESS_CLAMP;
        MipLODBias = 0;
        MaxAnisotropy = 1;
        ComparisonFunc = D3D11_COMPARISON_NEVER;
        BorderColor[ 0 ] = 1.0f;
        BorderColor[ 1 ] = 1.0f;
        BorderColor[ 2 ] = 1.0f;
        BorderColor[ 3 ] = 1.0f;
        MinLOD = -3.402823466e+38F; // -FLT_MAX
        MaxLOD = 3.402823466e+38F; // FLT_MAX
    }
    explicit CD3D11_SAMPLER_DESC(
        D3D11_FILTER filter,
        D3D11_TEXTURE_ADDRESS_MODE addressU,
        D3D11_TEXTURE_ADDRESS_MODE addressV,
        D3D11_TEXTURE_ADDRESS_MODE addressW,
        FLOAT mipLODBias,
        UINT maxAnisotropy,
        D3D11_COMPARISON_FUNC comparisonFunc,
        _In_reads_opt_( 4 ) const FLOAT* borderColor, // RGBA
        FLOAT minLOD,
        FLOAT maxLOD )
    {
        Filter = filter;
        AddressU = addressU;
        AddressV = addressV;
        AddressW = addressW;
        MipLODBias = mipLODBias;
        MaxAnisotropy = maxAnisotropy;
        ComparisonFunc = comparisonFunc;
        const float defaultColor[ 4 ] = { 1.0f, 1.0f, 1.0f, 1.0f };
        if (!borderColor) borderColor = defaultColor;
        BorderColor[ 0 ] = borderColor[ 0 ];
        BorderColor[ 1 ] = borderColor[ 1 ];
        BorderColor[ 2 ] = borderColor[ 2 ];
        BorderColor[ 3 ] = borderColor[ 3 ];
        MinLOD = minLOD;
        MaxLOD = maxLOD;
    }
    ~CD3D11_SAMPLER_DESC() {}
    operator const D3D11_SAMPLER_DESC&amp;() const { return *this; }
};
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/direct3d11/cd3d11-helper-classes">CD3D11 Helper Structures</a>