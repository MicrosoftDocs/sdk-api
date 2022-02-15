---
UID: NS:d3d11.CD3D11_SHADER_RESOURCE_VIEW_DESC
title: CD3D11_SHADER_RESOURCE_VIEW_DESC (d3d11.h)
description: Represents a shader-resource view and provides convenience methods for creating shader-resource views.
helpviewer_keywords: ["CD3D11_SHADER_RESOURCE_VIEW_DESC","CD3D11_SHADER_RESOURCE_VIEW_DESC structure [Direct3D 11]","d3d11/CD3D11_SHADER_RESOURCE_VIEW_DESC","direct3d11.cd3d11_shader_resource_view_desc"]
old-location: direct3d11\cd3d11_shader_resource_view_desc.htm
tech.root: direct3d11
ms.assetid: A6604A04-2D05-4CEB-8D47-C59789EE047E
ms.date: 12/05/2018
ms.keywords: CD3D11_SHADER_RESOURCE_VIEW_DESC, CD3D11_SHADER_RESOURCE_VIEW_DESC structure [Direct3D 11], d3d11/CD3D11_SHADER_RESOURCE_VIEW_DESC, direct3d11.cd3d11_shader_resource_view_desc
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
 - CD3D11_SHADER_RESOURCE_VIEW_DESC
 - d3d11/CD3D11_SHADER_RESOURCE_VIEW_DESC
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
 - CD3D11_SHADER_RESOURCE_VIEW_DESC
---

# CD3D11_SHADER_RESOURCE_VIEW_DESC structure


## -description

Represents a shader-resource view and provides convenience methods for creating shader-resource views.

## -struct-fields

## -remarks

Here is how D3D11.h defines <b>CD3D11_SHADER_RESOURCE_VIEW_DESC</b>:

<div class="code"><span><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
struct CD3D11_SHADER_RESOURCE_VIEW_DESC : public D3D11_SHADER_RESOURCE_VIEW_DESC
{
    CD3D11_SHADER_RESOURCE_VIEW_DESC()
    {}
    explicit CD3D11_SHADER_RESOURCE_VIEW_DESC( const D3D11_SHADER_RESOURCE_VIEW_DESC&amp; o ) :
        D3D11_SHADER_RESOURCE_VIEW_DESC( o )
    {}
    explicit CD3D11_SHADER_RESOURCE_VIEW_DESC(
        D3D11_SRV_DIMENSION viewDimension,
        DXGI_FORMAT format = DXGI_FORMAT_UNKNOWN,
        UINT mostDetailedMip = 0, // FirstElement for BUFFER
        UINT mipLevels = -1, // NumElements for BUFFER
        UINT firstArraySlice = 0, // First2DArrayFace for TEXTURECUBEARRAY
        UINT arraySize = -1, // NumCubes for TEXTURECUBEARRAY
        UINT flags = 0 ) // BUFFEREX only
    {
        Format = format;
        ViewDimension = viewDimension;
        switch (viewDimension)
        {
        case D3D11_SRV_DIMENSION_BUFFER:
            Buffer.FirstElement = mostDetailedMip;
            Buffer.NumElements = mipLevels;
            break;
        case D3D11_SRV_DIMENSION_TEXTURE1D:
            Texture1D.MostDetailedMip = mostDetailedMip;
            Texture1D.MipLevels = mipLevels;
            break;
        case D3D11_SRV_DIMENSION_TEXTURE1DARRAY:
            Texture1DArray.MostDetailedMip = mostDetailedMip;
            Texture1DArray.MipLevels = mipLevels;
            Texture1DArray.FirstArraySlice = firstArraySlice;
            Texture1DArray.ArraySize = arraySize;
            break;
        case D3D11_SRV_DIMENSION_TEXTURE2D:
            Texture2D.MostDetailedMip = mostDetailedMip;
            Texture2D.MipLevels = mipLevels;
            break;
        case D3D11_SRV_DIMENSION_TEXTURE2DARRAY:
            Texture2DArray.MostDetailedMip = mostDetailedMip;
            Texture2DArray.MipLevels = mipLevels;
            Texture2DArray.FirstArraySlice = firstArraySlice;
            Texture2DArray.ArraySize = arraySize;
            break;
        case D3D11_SRV_DIMENSION_TEXTURE2DMS:
            break;
        case D3D11_SRV_DIMENSION_TEXTURE2DMSARRAY:
            Texture2DMSArray.FirstArraySlice = firstArraySlice;
            Texture2DMSArray.ArraySize = arraySize;
            break;
        case D3D11_SRV_DIMENSION_TEXTURE3D:
            Texture3D.MostDetailedMip = mostDetailedMip;
            Texture3D.MipLevels = mipLevels;
            break;
        case D3D11_SRV_DIMENSION_TEXTURECUBE:
            TextureCube.MostDetailedMip = mostDetailedMip;
            TextureCube.MipLevels = mipLevels;
            break;
        case D3D11_SRV_DIMENSION_TEXTURECUBEARRAY:
            TextureCubeArray.MostDetailedMip = mostDetailedMip;
            TextureCubeArray.MipLevels = mipLevels;
            TextureCubeArray.First2DArrayFace = firstArraySlice;
            TextureCubeArray.NumCubes = arraySize;
            break;
        case D3D11_SRV_DIMENSION_BUFFEREX:
            BufferEx.FirstElement = mostDetailedMip;
            BufferEx.NumElements = mipLevels;
            BufferEx.Flags = flags;
            break;
        default: break;
        }
    }
    explicit CD3D11_SHADER_RESOURCE_VIEW_DESC(
        _In_ ID3D11Buffer*,
        DXGI_FORMAT format,
        UINT firstElement,
        UINT numElements,
        UINT flags = 0 )
    {
        Format = format;
        ViewDimension = D3D11_SRV_DIMENSION_BUFFEREX;
        BufferEx.FirstElement = firstElement;
        BufferEx.NumElements = numElements;
        BufferEx.Flags = flags;
    }
    explicit CD3D11_SHADER_RESOURCE_VIEW_DESC(
        _In_ ID3D11Texture1D* pTex1D,
        D3D11_SRV_DIMENSION viewDimension,
        DXGI_FORMAT format = DXGI_FORMAT_UNKNOWN,
        UINT mostDetailedMip = 0,
        UINT mipLevels = -1,
        UINT firstArraySlice = 0,
        UINT arraySize = -1 )
    {
        ViewDimension = viewDimension;
        if (DXGI_FORMAT_UNKNOWN == format || -1 == mipLevels ||
            (-1 == arraySize &amp;&amp; D3D11_SRV_DIMENSION_TEXTURE1DARRAY == viewDimension))
        {
            D3D11_TEXTURE1D_DESC TexDesc;
            pTex1D-&gt;GetDesc( &amp;TexDesc );
            if (DXGI_FORMAT_UNKNOWN == format) format = TexDesc.Format;
            if (-1 == mipLevels) mipLevels = TexDesc.MipLevels - mostDetailedMip;
            if (-1 == arraySize) arraySize = TexDesc.ArraySize - firstArraySlice;
        }
        Format = format;
        switch (viewDimension)
        {
        case D3D11_SRV_DIMENSION_TEXTURE1D:
            Texture1D.MostDetailedMip = mostDetailedMip;
            Texture1D.MipLevels = mipLevels;
            break;
        case D3D11_SRV_DIMENSION_TEXTURE1DARRAY:
            Texture1DArray.MostDetailedMip = mostDetailedMip;
            Texture1DArray.MipLevels = mipLevels;
            Texture1DArray.FirstArraySlice = firstArraySlice;
            Texture1DArray.ArraySize = arraySize;
            break;
        default: break;
        }
    }
    explicit CD3D11_SHADER_RESOURCE_VIEW_DESC(
        _In_ ID3D11Texture2D* pTex2D,
        D3D11_SRV_DIMENSION viewDimension,
        DXGI_FORMAT format = DXGI_FORMAT_UNKNOWN,
        UINT mostDetailedMip = 0,
        UINT mipLevels = -1,
        UINT firstArraySlice = 0, // First2DArrayFace for TEXTURECUBEARRAY
        UINT arraySize = -1 ) // NumCubes for TEXTURECUBEARRAY
    {
        ViewDimension = viewDimension;
        if (DXGI_FORMAT_UNKNOWN == format || 
            (-1 == mipLevels &amp;&amp;
                D3D11_SRV_DIMENSION_TEXTURE2DMS != viewDimension &amp;&amp;
                D3D11_SRV_DIMENSION_TEXTURE2DMSARRAY != viewDimension) ||
            (-1 == arraySize &amp;&amp;
                (D3D11_SRV_DIMENSION_TEXTURE2DARRAY == viewDimension ||
                D3D11_SRV_DIMENSION_TEXTURE2DMSARRAY == viewDimension ||
                D3D11_SRV_DIMENSION_TEXTURECUBEARRAY == viewDimension)))
        {
            D3D11_TEXTURE2D_DESC TexDesc;
            pTex2D-&gt;GetDesc( &amp;TexDesc );
            if (DXGI_FORMAT_UNKNOWN == format) format = TexDesc.Format;
            if (-1 == mipLevels) mipLevels = TexDesc.MipLevels - mostDetailedMip;
            if (-1 == arraySize)
            {
                arraySize = TexDesc.ArraySize - firstArraySlice;
                if (D3D11_SRV_DIMENSION_TEXTURECUBEARRAY == viewDimension) arraySize /= 6;
            }
        }
        Format = format;
        switch (viewDimension)
        {
        case D3D11_SRV_DIMENSION_TEXTURE2D:
            Texture2D.MostDetailedMip = mostDetailedMip;
            Texture2D.MipLevels = mipLevels;
            break;
        case D3D11_SRV_DIMENSION_TEXTURE2DARRAY:
            Texture2DArray.MostDetailedMip = mostDetailedMip;
            Texture2DArray.MipLevels = mipLevels;
            Texture2DArray.FirstArraySlice = firstArraySlice;
            Texture2DArray.ArraySize = arraySize;
            break;
        case D3D11_SRV_DIMENSION_TEXTURE2DMS:
            break;
        case D3D11_SRV_DIMENSION_TEXTURE2DMSARRAY:
            Texture2DMSArray.FirstArraySlice = firstArraySlice;
            Texture2DMSArray.ArraySize = arraySize;
            break;
        case D3D11_SRV_DIMENSION_TEXTURECUBE:
            TextureCube.MostDetailedMip = mostDetailedMip;
            TextureCube.MipLevels = mipLevels;
            break;
        case D3D11_SRV_DIMENSION_TEXTURECUBEARRAY:
            TextureCubeArray.MostDetailedMip = mostDetailedMip;
            TextureCubeArray.MipLevels = mipLevels;
            TextureCubeArray.First2DArrayFace = firstArraySlice;
            TextureCubeArray.NumCubes = arraySize;
            break;
        default: break;
        }
    }
    explicit CD3D11_SHADER_RESOURCE_VIEW_DESC(
        _In_ ID3D11Texture3D* pTex3D,
        DXGI_FORMAT format = DXGI_FORMAT_UNKNOWN,
        UINT mostDetailedMip = 0,
        UINT mipLevels = -1 )
    {
        ViewDimension = D3D11_SRV_DIMENSION_TEXTURE3D;
        if (DXGI_FORMAT_UNKNOWN == format || -1 == mipLevels)
        {
            D3D11_TEXTURE3D_DESC TexDesc;
            pTex3D-&gt;GetDesc( &amp;TexDesc );
            if (DXGI_FORMAT_UNKNOWN == format) format = TexDesc.Format;
            if (-1 == mipLevels) mipLevels = TexDesc.MipLevels - mostDetailedMip;
        }
        Format = format;
        Texture3D.MostDetailedMip = mostDetailedMip;
        Texture3D.MipLevels = mipLevels;
    }
    ~CD3D11_SHADER_RESOURCE_VIEW_DESC() {}
    operator const D3D11_SHADER_RESOURCE_VIEW_DESC&amp;() const { return *this; }
};</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/direct3d11/cd3d11-helper-classes">CD3D11 Helper Structures</a>