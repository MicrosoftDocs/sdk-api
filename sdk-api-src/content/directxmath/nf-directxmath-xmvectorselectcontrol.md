---
UID: NF:directxmath.XMVectorSelectControl
title: XMVectorSelectControl function (directxmath.h)
description: Defines a control vector for use in XMVectorSelect.
helpviewer_keywords: ["Use DirectX..XMVectorSelectControl","XMVectorSelectControl","XMVectorSelectControl method [DirectX Math Support APIs]","dxmath.xmvectorselectcontrol"]
old-location: dxmath\xmvectorselectcontrol.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.component-wise.XMVectorSelectControl(uint32_t,uint32_t,uint32_t,uint32_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSelectControl, XMVectorSelectControl, XMVectorSelectControl method [DirectX Math Support APIs], dxmath.xmvectorselectcontrol
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
 - XMVectorSelectControl
 - directxmath/XMVectorSelectControl
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
 - XMVectorSelectControl
---

# XMVectorSelectControl function


## -description

Defines a control vector for use in <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselect">XMVectorSelect</a>.

## -parameters

### -param VectorIndex0 [in]

Index that determines which vector in <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselect">XMVectorSelect</a> will be selected. If zero, the first vector's first component will be selected. Otherwise, the second vector's component will be selected.

### -param VectorIndex1 [in]

Index that determines which vector in <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselect">XMVectorSelect</a> will be selected. If zero, the first vector's second component will be selected. Otherwise, the second vector's component will be selected.

### -param VectorIndex2 [in]

Index that determines which vector in <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselect">XMVectorSelect</a> will be selected. If zero, the first vector's third component will be selected. Otherwise, the second vector's component will be selected.

### -param VectorIndex3 [in]

Index that determines which vector in <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselect">XMVectorSelect</a> will be selected. If zero, the first vector's fourth component will be selected. Otherwise, the second vector's component will be selected.

## -returns

Returns the control vector.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR    ControlVector;
const uint32_t  ControlElement[] =
            {
                XM_SELECT_0,
                XM_SELECT_1
            };

assert(VectorIndex0 < 2);
assert(VectorIndex1 < 2);
assert(VectorIndex2 < 2);
assert(VectorIndex3 < 2);

ControlVector.u[0] = ControlElement[VectorIndex0];
ControlVector.u[1] = ControlElement[VectorIndex1];
ControlVector.u[2] = ControlElement[VectorIndex2];
ControlVector.u[3] = ControlElement[VectorIndex3];

return ControlVector;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.


#### Examples

Using XMVectorSelectControl

In this example, <b>XMVectorSelectControl</b> is used to generate a control mask that will select the x and w components from the first vector and the y and z components from the second.

The vector result will be ( 3.0f, 5.0f, 5.0f, 3.0f ).


```
XMVECTOR three = XMVectorReplicate( 3.0f );
XMVECTOR five = XMVectorReplicate( 5.0f );

XMVECTOR control = XMVectorSelectControl( 0, 1, 1, 0 );
XMVECTOR result = XMVectorSelect( three, five, control );
```

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-component-wise">Component-Wise Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselect">XMVectorSelect</a>