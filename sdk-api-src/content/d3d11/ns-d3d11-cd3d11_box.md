---
UID: NS:d3d11.CD3D11_BOX
title: CD3D11_BOX (d3d11.h)
description: Represents a box and provides convenience methods for creating boxes.
helpviewer_keywords: ["CD3D11_BOX","CD3D11_BOX structure [Direct3D 11]","d3d11/CD3D11_BOX","direct3d11.cd3d11_box"]
old-location: direct3d11\cd3d11_box.htm
tech.root: direct3d11
ms.assetid: 5ACD1DB9-FB35-48F4-8533-3B7464CF5F3D
ms.date: 12/05/2018
ms.keywords: CD3D11_BOX, CD3D11_BOX structure [Direct3D 11], d3d11/CD3D11_BOX, direct3d11.cd3d11_box
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
 - CD3D11_BOX
 - d3d11/CD3D11_BOX
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
 - CD3D11_BOX
---

# CD3D11_BOX structure


## -description

Represents a box and provides convenience methods for creating boxes.

## -struct-fields

## -remarks

Here is how D3D11.h defines <b>CD3D11_BOX</b>:

<div class="code"><span><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
struct CD3D11_BOX : public D3D11_BOX
{
    CD3D11_BOX()
    {}
    explicit CD3D11_BOX( const D3D11_BOX&amp; o ) :
        D3D11_BOX( o )
    {}
    explicit CD3D11_BOX(
        LONG Left,
        LONG Top,
        LONG Front,
        LONG Right,
        LONG Bottom,
        LONG Back )
    {
        left = Left;
        top = Top;
        front = Front;
        right = Right;
        bottom = Bottom;
        back = Back;
    }
    ~CD3D11_BOX() {}
    operator const D3D11_BOX&amp;() const { return *this; }
};
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/direct3d11/cd3d11-helper-classes">CD3D11 Helper Structures</a>