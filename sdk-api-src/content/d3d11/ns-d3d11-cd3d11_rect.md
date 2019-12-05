---
UID: NS:d3d11.CD3D11_RECT
title: CD3D11_RECT (d3d11.h)
description: Represents a rectangle and provides convenience methods for creating rectangles.
old-location: direct3d11\cd3d11_rect.htm
tech.root: direct3d11
ms.assetid: 737B47A3-E609-48E4-A0B6-017206E500B1
ms.date: 12/05/2018
ms.keywords: CD3D11_RECT, CD3D11_RECT structure [Direct3D 11], d3d11/CD3D11_RECT, direct3d11.cd3d11_rect
ms.topic: struct
f1_keywords:
- d3d11/CD3D11_RECT
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
- CD3D11_RECT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CD3D11_RECT structure


## -description


Represents a rectangle and provides convenience methods for creating rectangles.


## -struct-fields


## -remarks



Here is how D3D11.h defines <b>CD3D11_RECT</b>:


<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>struct CD3D11_RECT : public D3D11_RECT
{
    CD3D11_RECT()
    {}
    explicit CD3D11_RECT( const D3D11_RECT&amp; o ) :
        D3D11_RECT( o )
    {}
    explicit CD3D11_RECT(
        LONG Left,
        LONG Top,
        LONG Right,
        LONG Bottom )
    {
        left = Left;
        top = Top;
        right = Right;
        bottom = Bottom;
    }
    ~CD3D11_RECT() {}
    operator const D3D11_RECT&amp;() const { return *this; }
};
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/cd3d11-helper-classes">CD3D11 Helper Structures</a>
 

 

