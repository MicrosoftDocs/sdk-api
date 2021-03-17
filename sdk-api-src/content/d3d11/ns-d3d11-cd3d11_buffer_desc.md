---
UID: NS:d3d11.CD3D11_BUFFER_DESC
title: CD3D11_BUFFER_DESC (d3d11.h)
description: Represents a buffer and provides convenience methods for creating buffers.
helpviewer_keywords: ["CD3D11_BUFFER_DESC","CD3D11_BUFFER_DESC structure [Direct3D 11]","d3d11/CD3D11_BUFFER_DESC","direct3d11.cd3d11_buffer_desc"]
old-location: direct3d11\cd3d11_buffer_desc.htm
tech.root: direct3d11
ms.assetid: A6ED5755-AB4A-4C35-A344-1693D78F7A4B
ms.date: 12/05/2018
ms.keywords: CD3D11_BUFFER_DESC, CD3D11_BUFFER_DESC structure [Direct3D 11], d3d11/CD3D11_BUFFER_DESC, direct3d11.cd3d11_buffer_desc
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
 - CD3D11_BUFFER_DESC
 - d3d11/CD3D11_BUFFER_DESC
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
 - CD3D11_BUFFER_DESC
---

# CD3D11_BUFFER_DESC structure


## -description

Represents a buffer and provides convenience methods for creating buffers.

## -struct-fields

### -field CD3D11_BUFFER_DESC

TBD

### -field ~CD3D11_BUFFER_DESC

TBD

### -field operator const D3D11_BUFFER_DESC&

TBD

### -field D3D11_BUFFER_DESC

 




##### - See Below.

## -remarks

Here is how D3D11.h defines <b>CD3D11_BUFFER_DESC</b>:


```

struct CD3D11_BUFFER_DESC : public D3D11_BUFFER_DESC
{
    CD3D11_BUFFER_DESC()
    {}
    explicit CD3D11_BUFFER_DESC( const D3D11_BUFFER_DESC& o ) :
        D3D11_BUFFER_DESC( o )
    {}
    explicit CD3D11_BUFFER_DESC(
        UINT byteWidth,
        UINT bindFlags,
        D3D11_USAGE usage = D3D11_USAGE_DEFAULT,
        UINT cpuaccessFlags = 0,
        UINT miscFlags = 0,
        UINT structureByteStride = 0 )
    {
        ByteWidth = byteWidth;
        Usage = usage;
        BindFlags = bindFlags;
        CPUAccessFlags = cpuaccessFlags ;
        MiscFlags = miscFlags;
        StructureByteStride = structureByteStride;
    }
    ~CD3D11_BUFFER_DESC() {}
    operator const D3D11_BUFFER_DESC&() const { return *this; }
};

```

## -see-also

<a href="/windows/desktop/direct3d11/cd3d11-helper-classes">CD3D11 Helper Structures</a>