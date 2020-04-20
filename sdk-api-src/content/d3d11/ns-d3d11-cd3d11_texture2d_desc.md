---
UID: NS:d3d11.CD3D11_TEXTURE2D_DESC
title: CD3D11_TEXTURE2D_DESC (d3d11.h)
description: Represents a 2D texture and provides convenience methods for creating 2D textures.helpviewer_keywords: ["CD3D11_TEXTURE2D_DESC","CD3D11_TEXTURE2D_DESC structure [Direct3D 11]","d3d11/CD3D11_TEXTURE2D_DESC","direct3d11.cd3d11_texture2d_desc"]
old-location: direct3d11\cd3d11_texture2d_desc.htm
tech.root: direct3d11
ms.assetid: BD0FB68A-17DF-412C-9CAD-26D95AF2E16F
ms.date: 12/05/2018
ms.keywords: CD3D11_TEXTURE2D_DESC, CD3D11_TEXTURE2D_DESC structure [Direct3D 11], d3d11/CD3D11_TEXTURE2D_DESC, direct3d11.cd3d11_texture2d_desc
f1_keywords:
- d3d11/CD3D11_TEXTURE2D_DESC
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- D3D11.h
api_name:
- CD3D11_TEXTURE2D_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CD3D11_TEXTURE2D_DESC structure


## -description


Represents a 2D texture and provides convenience methods for creating 2D textures.


## -struct-fields


## -remarks



Here is how D3D11.h defines <b>CD3D11_TEXTURE2D_DESC</b>:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
struct CD3D11_TEXTURE2D_DESC : public D3D11_TEXTURE2D_DESC
{
    CD3D11_TEXTURE2D_DESC()
    {}
    explicit CD3D11_TEXTURE2D_DESC( const D3D11_TEXTURE2D_DESC&amp; o ) :
        D3D11_TEXTURE2D_DESC( o )
    {}
    explicit CD3D11_TEXTURE2D_DESC(
        DXGI_FORMAT format,
        UINT width,
        UINT height,
        UINT arraySize = 1,
        UINT mipLevels = 0,
        UINT bindFlags = D3D11_BIND_SHADER_RESOURCE,
        D3D11_USAGE usage = D3D11_USAGE_DEFAULT,
        UINT cpuaccessFlags = 0,
        UINT sampleCount = 1,
        UINT sampleQuality = 0,
        UINT miscFlags = 0 )
    {
        Width = width;
        Height = height;
        MipLevels = mipLevels;
        ArraySize = arraySize;
        Format = format;
        SampleDesc.Count = sampleCount;
        SampleDesc.Quality = sampleQuality;
        Usage = usage;
        BindFlags = bindFlags;
        CPUAccessFlags = cpuaccessFlags;
        MiscFlags = miscFlags;
    }
    ~CD3D11_TEXTURE2D_DESC() {}
    operator const D3D11_TEXTURE2D_DESC&amp;() const { return *this; }
};
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/cd3d11-helper-classes">CD3D11 Helper Structures</a>
 

 

