---
UID: NS:d3d11.CD3D11_UNORDERED_ACCESS_VIEW_DESC
title: CD3D11_UNORDERED_ACCESS_VIEW_DESC (d3d11.h)
description: Represents a unordered-access view and provides convenience methods for creating unordered-access views.
helpviewer_keywords: ["CD3D11_UNORDERED_ACCESS_VIEW_DESC","CD3D11_UNORDERED_ACCESS_VIEW_DESC structure [Direct3D 11]","d3d11/CD3D11_UNORDERED_ACCESS_VIEW_DESC","direct3d11.cd3d11_unordered_access_view_desc"]
old-location: direct3d11\cd3d11_unordered_access_view_desc.htm
tech.root: direct3d11
ms.assetid: 8062BFAB-4A68-4ED4-B82F-0D1FF9E81733
ms.date: 12/05/2018
ms.keywords: CD3D11_UNORDERED_ACCESS_VIEW_DESC, CD3D11_UNORDERED_ACCESS_VIEW_DESC structure [Direct3D 11], d3d11/CD3D11_UNORDERED_ACCESS_VIEW_DESC, direct3d11.cd3d11_unordered_access_view_desc
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
 - CD3D11_UNORDERED_ACCESS_VIEW_DESC
 - d3d11/CD3D11_UNORDERED_ACCESS_VIEW_DESC
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
 - CD3D11_UNORDERED_ACCESS_VIEW_DESC
---

# CD3D11_UNORDERED_ACCESS_VIEW_DESC structure


## -description

Represents a unordered-access view and provides convenience methods for creating unordered-access views.

## -struct-fields

## -remarks

Here is how D3D11.h defines <b>CD3D11_UNORDERED_ACCESS_VIEW_DESC</b>:

<div class="code"><span><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
struct CD3D11_UNORDERED_ACCESS_VIEW_DESC : public D3D11_UNORDERED_ACCESS_VIEW_DESC
{
    CD3D11_UNORDERED_ACCESS_VIEW_DESC()
    {}
    explicit CD3D11_UNORDERED_ACCESS_VIEW_DESC( const D3D11_UNORDERED_ACCESS_VIEW_DESC&amp; o ) :
        D3D11_UNORDERED_ACCESS_VIEW_DESC( o )
    {}
    explicit CD3D11_UNORDERED_ACCESS_VIEW_DESC(
        D3D11_UAV_DIMENSION viewDimension,
        DXGI_FORMAT format = DXGI_FORMAT_UNKNOWN,
        UINT mipSlice = 0, // FirstElement for BUFFER
        UINT firstArraySlice = 0, // NumElements for BUFFER, FirstWSlice for TEXTURE3D
        UINT arraySize = -1, // WSize for TEXTURE3D
        UINT flags = 0 ) // BUFFER only
    {
        Format = format;
        ViewDimension = viewDimension;
        switch (viewDimension)
        {
        case D3D11_UAV_DIMENSION_BUFFER:
            Buffer.FirstElement = mipSlice;
            Buffer.NumElements = firstArraySlice;
            Buffer.Flags = flags;
            break;
        case D3D11_UAV_DIMENSION_TEXTURE1D:
            Texture1D.MipSlice = mipSlice;
            break;
        case D3D11_UAV_DIMENSION_TEXTURE1DARRAY:
            Texture1DArray.MipSlice = mipSlice;
            Texture1DArray.FirstArraySlice = firstArraySlice;
            Texture1DArray.ArraySize = arraySize;
            break;
        case D3D11_UAV_DIMENSION_TEXTURE2D:
            Texture2D.MipSlice = mipSlice;
            break;
        case D3D11_UAV_DIMENSION_TEXTURE2DARRAY:
            Texture2DArray.MipSlice = mipSlice;
            Texture2DArray.FirstArraySlice = firstArraySlice;
            Texture2DArray.ArraySize = arraySize;
            break;
        case D3D11_UAV_DIMENSION_TEXTURE3D:
            Texture3D.MipSlice = mipSlice;
            Texture3D.FirstWSlice = firstArraySlice;
            Texture3D.WSize = arraySize;
            break;
        default: break;
        }
    }
    explicit CD3D11_UNORDERED_ACCESS_VIEW_DESC(
        _In_ ID3D11Buffer*,
        DXGI_FORMAT format,
        UINT firstElement,
        UINT numElements,
        UINT flags = 0 )
    {
        Format = format;
        ViewDimension = D3D11_UAV_DIMENSION_BUFFER;
        Buffer.FirstElement = firstElement;
        Buffer.NumElements = numElements;
        Buffer.Flags = flags;
    }
    explicit CD3D11_UNORDERED_ACCESS_VIEW_DESC(
        _In_ ID3D11Texture1D* pTex1D,
        D3D11_UAV_DIMENSION viewDimension,
        DXGI_FORMAT format = DXGI_FORMAT_UNKNOWN,
        UINT mipSlice = 0,
        UINT firstArraySlice = 0,
        UINT arraySize = -1 )
    {
        ViewDimension = viewDimension;
        if (DXGI_FORMAT_UNKNOWN == format ||
            (-1 == arraySize &amp;&amp; D3D11_UAV_DIMENSION_TEXTURE1DARRAY == viewDimension))
        {
            D3D11_TEXTURE1D_DESC TexDesc;
            pTex1D-&gt;GetDesc( &amp;TexDesc );
            if (DXGI_FORMAT_UNKNOWN == format) format = TexDesc.Format;
            if (-1 == arraySize) arraySize = TexDesc.ArraySize - firstArraySlice;
        }
        Format = format;
        switch (viewDimension)
        {
        case D3D11_UAV_DIMENSION_TEXTURE1D:
            Texture1D.MipSlice = mipSlice;
            break;
        case D3D11_UAV_DIMENSION_TEXTURE1DARRAY:
            Texture1DArray.MipSlice = mipSlice;
            Texture1DArray.FirstArraySlice = firstArraySlice;
            Texture1DArray.ArraySize = arraySize;
            break;
        default: break;
        }
    }
    explicit CD3D11_UNORDERED_ACCESS_VIEW_DESC(
        _In_ ID3D11Texture2D* pTex2D,
        D3D11_UAV_DIMENSION viewDimension,
        DXGI_FORMAT format = DXGI_FORMAT_UNKNOWN,
        UINT mipSlice = 0,
        UINT firstArraySlice = 0,
        UINT arraySize = -1 )
    {
        ViewDimension = viewDimension;
        if (DXGI_FORMAT_UNKNOWN == format || 
            (-1 == arraySize &amp;&amp; D3D11_UAV_DIMENSION_TEXTURE2DARRAY == viewDimension))
        {
            D3D11_TEXTURE2D_DESC TexDesc;
            pTex2D-&gt;GetDesc( &amp;TexDesc );
            if (DXGI_FORMAT_UNKNOWN == format) format = TexDesc.Format;
            if (-1 == arraySize) arraySize = TexDesc.ArraySize - firstArraySlice;
        }
        Format = format;
        switch (viewDimension)
        {
        case D3D11_UAV_DIMENSION_TEXTURE2D:
            Texture2D.MipSlice = mipSlice;
            break;
        case D3D11_UAV_DIMENSION_TEXTURE2DARRAY:
            Texture2DArray.MipSlice = mipSlice;
            Texture2DArray.FirstArraySlice = firstArraySlice;
            Texture2DArray.ArraySize = arraySize;
            break;
        default: break;
        }
    }
    explicit CD3D11_UNORDERED_ACCESS_VIEW_DESC(
        _In_ ID3D11Texture3D* pTex3D,
        DXGI_FORMAT format = DXGI_FORMAT_UNKNOWN,
        UINT mipSlice = 0,
        UINT firstWSlice = 0,
        UINT wSize = -1 )
    {
        ViewDimension = D3D11_UAV_DIMENSION_TEXTURE3D;
        if (DXGI_FORMAT_UNKNOWN == format || -1 == wSize)
        {
            D3D11_TEXTURE3D_DESC TexDesc;
            pTex3D-&gt;GetDesc( &amp;TexDesc );
            if (DXGI_FORMAT_UNKNOWN == format) format = TexDesc.Format;
            if (-1 == wSize) wSize = TexDesc.Depth - firstWSlice;
        }
        Format = format;
        Texture3D.MipSlice = mipSlice;
        Texture3D.FirstWSlice = firstWSlice;
        Texture3D.WSize = wSize;
    }
    ~CD3D11_UNORDERED_ACCESS_VIEW_DESC() {}
    operator const D3D11_UNORDERED_ACCESS_VIEW_DESC&amp;() const { return *this; }
};
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/direct3d11/cd3d11-helper-classes">CD3D11 Helper Structures</a>