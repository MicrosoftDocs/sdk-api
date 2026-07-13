---
UID: NF:directxmath.XMVectorShiftLeft
title: XMVectorShiftLeft function (directxmath.h)
description: Shifts a vector left by a given number of 32-bit elements, filling the vacated elements with elements from a second vector.
helpviewer_keywords: ["Use DirectX..XMVectorShiftLeft","XMVectorShiftLeft","XMVectorShiftLeft method [DirectX Math Support APIs]","dxmath.xmvectorshiftleft"]
old-location: dxmath\xmvectorshiftleft.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.component-wise.XMVectorShiftLeft(XMVECTOR,XMVECTOR,uint32_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorShiftLeft, XMVectorShiftLeft, XMVectorShiftLeft method [DirectX Math Support APIs], dxmath.xmvectorshiftleft
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
 - XMVectorShiftLeft
 - directxmath/XMVectorShiftLeft
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
 - XMVectorShiftLeft
---

# XMVectorShiftLeft function


## -description

Shifts a vector left by a given number of 32-bit elements, filling the vacated elements with elements from a second
  vector.

## -parameters

### -param V1 [in]

Vector to shift left.

### -param V2 [in]

Vector used to fill in the vacated components of <i>V1</i> after it is shifted left.

### -param Elements [in]

Number of 32-bit elements by which to shift <i>V</i> left. This parameter must be 0, 1, 2, or 3.

## -returns

Returns the shifted and filled in <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a>.

## -remarks

The following code demonstrates how this function might be used.


```
XMVECTOR v1 = XMVectorSet( 10.0f, 20.0f, 30.0f, 40.0f );
XMVECTOR v2 = XMVectorSet( 50.0f, 60.0f, 70.0f, 80.0f );
XMVECTOR result = XMVectorShiftLeft( v1, v2, 1 );
```


The shifted vector (<i>result</i>) will be &lt;20.0f, 30.0f, 40.0f, 50.0f&gt;.

In the case of a constant shift value, it is more efficient to use the template form of <a href="/windows/desktop/dxmath/xmvectorshiftleft-template">XMVectorShiftLeft</a>:


```

template<uint32_t Elements>
    XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)

Example: XMVectorShiftLeft<1>( v1, v2 );
   
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-component-wise">Component-Wise Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorpermute">XMVectorPermute</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorrotateleft">XMVectorRotateLeft</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorrotateright">XMVectorRotateRight</a>