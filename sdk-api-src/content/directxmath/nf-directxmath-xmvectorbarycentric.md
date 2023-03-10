---
UID: NF:directxmath.XMVectorBaryCentric
title: XMVectorBaryCentric function (directxmath.h)
description: Returns a point in Barycentric coordinates, using the specified position vectors. (XMVectorBaryCentric)
helpviewer_keywords: ["Use DirectX..XMVectorBaryCentric","XMVectorBaryCentric","XMVectorBaryCentric method [DirectX Math Support APIs]","dxmath.xmvectorbarycentric"]
old-location: dxmath\xmvectorbarycentric.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVectorBaryCentric(XMVECTOR,XMVECTOR,XMVECTOR,float,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorBaryCentric, XMVectorBaryCentric, XMVectorBaryCentric method [DirectX Math Support APIs], dxmath.xmvectorbarycentric
req.header: directxmath.h
req.include-header: DirectXMath.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: Use DirectX.
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
 - XMVectorBaryCentric
 - directxmath/XMVectorBaryCentric
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxmathvector.inl
api_name:
 - XMVectorBaryCentric
---

# XMVectorBaryCentric function


## -description

Returns a point in Barycentric coordinates, using the specified position vectors.

## -parameters

### -param Position0 [in]

First position.

### -param Position1 [in]

Second position.

### -param Position2 [in]

Third position.

### -param f [in]

Weighting factor. See the remarks.

### -param g [in]

Weighting factor. See the remarks.

## -returns

Returns the Barycentric coordinates.

## -remarks

This function provides a way to understand points in and around a triangle, independent of where the triangle is located. This function returns the resulting point by using the following equation: <i>Position0</i>&gt; + <i>f</i>&gt;(<i>Position1</i>-<i>Position0</i>&gt;) + <i>g</i>&gt;(<i>Position2</i>-<i>Position0</i>&gt;). 

Any point in the plane <i>Position0</i>&gt;<i>Position1</i>&gt;<i>Position2</i>&gt; can be represented by the Barycentric coordinate (<i>f</i>&gt;,<i>g</i>&gt;), where <i>f</i>&gt; controls how much <i>Position1</i>&gt; gets weighted into the result, and <i>g</i>&gt; controls how much <i>Position2</i>&gt; gets weighted into the result. Lastly, 1-<i>f</i>&gt;-<i>g</i>&gt; controls how much <i>Position0</i>&gt; gets weighted into the result.

Note the following relations. 

<ul>
<li>
If (<i>f</i>&gt;=0 &amp;&amp; <i>g</i>&gt;=0 &amp;&amp; 1-<i>f</i>-<i>g</i>&gt;=0), the point is inside the triangle <i>Position0</i>&gt;<i>Position1</i>&gt;<i>Position2</i>&gt;. 

</li>
<li>
If (<i>f</i>==0 &amp;&amp; <i>g</i>&gt;=0 &amp;&amp; 1-<i>f</i>-<i>g</i>&gt;=0), the point is on the line <i>Position0</i>&gt;<i>Position2</i>&gt;. 

</li>
<li>
If (<i>f</i>&gt;=0 &amp;&amp; <i>g</i>==0 &amp;&amp; 1-<i>f</i>-g&gt;=0), the point is on the line <i>Position0</i>&gt;<i>Position1</i>&gt;. 

</li>
<li>
If (<i>f</i>&gt;=0 &amp;&amp; <i>g</i>&gt;=0 &amp;&amp; 1-<i>f</i>-<i>g</i>==0), the point is on the line <i>Position1</i>&gt;<i>Position2</i>&gt;. 

</li>
</ul>
Barycentric coordinates are a form of general coordinates. In this context, using Barycentric coordinates represents a change in coordinate systems. What holds true for Cartesian coordinates holds true for Barycentric coordinates.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-geometric">Geometric Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorbarycentricv">XMVectorBaryCentricV</a>
