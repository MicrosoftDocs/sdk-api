---
UID: NS:d3d11.CD3D11_QUERY_DESC
title: CD3D11_QUERY_DESC (d3d11.h)
description: Represents a query and provides convenience methods for creating queries.
helpviewer_keywords: ["CD3D11_QUERY_DESC","CD3D11_QUERY_DESC structure [Direct3D 11]","d3d11/CD3D11_QUERY_DESC","direct3d11.cd3d11_query_desc"]
old-location: direct3d11\cd3d11_query_desc.htm
tech.root: direct3d11
ms.assetid: F77E6197-550F-47ED-9619-42C8D2F16AF5
ms.date: 12/05/2018
ms.keywords: CD3D11_QUERY_DESC, CD3D11_QUERY_DESC structure [Direct3D 11], d3d11/CD3D11_QUERY_DESC, direct3d11.cd3d11_query_desc
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
 - CD3D11_QUERY_DESC
 - d3d11/CD3D11_QUERY_DESC
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
 - CD3D11_QUERY_DESC
---

# CD3D11_QUERY_DESC structure


## -description

Represents a query and provides convenience methods for creating queries.

## -struct-fields

## -remarks

Here is how D3D11.h defines <b>CD3D11_QUERY_DESC</b>:

<div class="code"><span><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
struct CD3D11_QUERY_DESC : public D3D11_QUERY_DESC
{
    CD3D11_QUERY_DESC()
    {}
    explicit CD3D11_QUERY_DESC( const D3D11_QUERY_DESC&amp; o ) :
        D3D11_QUERY_DESC( o )
    {}
    explicit CD3D11_QUERY_DESC(
        D3D11_QUERY query,
        UINT miscFlags = 0 )
    {
        Query = query;
        MiscFlags = miscFlags;
    }
    ~CD3D11_QUERY_DESC() {}
    operator const D3D11_QUERY_DESC&amp;() const { return *this; }
};
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/direct3d11/cd3d11-helper-classes">CD3D11 Helper Structures</a>