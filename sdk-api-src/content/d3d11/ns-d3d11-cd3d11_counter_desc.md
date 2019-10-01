---
UID: NS:d3d11.CD3D11_COUNTER_DESC
title: CD3D11_COUNTER_DESC (d3d11.h)
author: windows-sdk-content
description: Represents a counter and provides convenience methods for creating counters.
old-location: direct3d11\cd3d11_counter_desc.htm
tech.root: direct3d11
ms.assetid: 7625F9B4-B181-44B3-BA1F-46936EF151DE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CD3D11_COUNTER_DESC, CD3D11_COUNTER_DESC structure [Direct3D 11], d3d11/CD3D11_COUNTER_DESC, direct3d11.cd3d11_counter_desc
ms.topic: struct
f1_keywords: 
 - "d3d11/CD3D11_COUNTER_DESC"
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
 - CD3D11_COUNTER_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CD3D11_COUNTER_DESC structure


## -description


Represents a counter and provides convenience methods for creating counters.


## -struct-fields


## -remarks



Here is how D3D11.h defines <b>CD3D11_COUNTER_DESC</b>:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
struct CD3D11_COUNTER_DESC : public D3D11_COUNTER_DESC
{
    CD3D11_COUNTER_DESC()
    {}
    explicit CD3D11_COUNTER_DESC( const D3D11_COUNTER_DESC&amp; o ) :
        D3D11_COUNTER_DESC( o )
    {}
    explicit CD3D11_COUNTER_DESC(
        D3D11_COUNTER counter,
        UINT miscFlags = 0 )
    {
        Counter = counter;
        MiscFlags = miscFlags;
    }
    ~CD3D11_COUNTER_DESC() {}
    operator const D3D11_COUNTER_DESC&amp;() const { return *this; }
};
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/cd3d11-helper-classes">CD3D11 Helper Structures</a>
 

 

