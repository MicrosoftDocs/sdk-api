---
UID: NF:directxmath.XMVectorSelect
title: XMVectorSelect function (directxmath.h)
description: Performs a per-component selection between two input vectors and returns the resulting vector.
helpviewer_keywords: ["Use DirectX..XMVectorSelect","XMVectorSelect","XMVectorSelect method [DirectX Math Support APIs]","dxmath.xmvectorselect"]
old-location: dxmath\xmvectorselect.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.component-wise.XMVectorSelect(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSelect, XMVectorSelect, XMVectorSelect method [DirectX Math Support APIs], dxmath.xmvectorselect
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
 - XMVectorSelect
 - directxmath/XMVectorSelect
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
 - XMVectorSelect
---

# XMVectorSelect function


## -description

Performs a per-component selection between two input vectors and returns the resulting vector.

## -parameters

### -param V1 [in]

First vector to compare.

### -param V2 [in]

Second vector to compare.

### -param Control [in]

Vector mask used to select a vector component from either <i>V1</i> or <i>V2</i>. If a component of
        <i>Control</i> is zero, the returned vector's corresponding component will be the first vector's component.
        If a component of <i>Control</i> is 0xFF, the returned vector's corresponding component will be the second
        vector's component. For full details on how the vector mask works, see the "Remarks".

Typically, the vector used for <i>Control</i> will be either the output of a vector comparison function (such as
        <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorequal">XMVectorEqual</a>,
        <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorless">XMVectorLess</a>, or
        <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorgreater">XMVectorGreater</a>) or it will be the output
        of <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselectcontrol">XMVectorSelectControl</a>.

## -returns

Returns the result of the per-component selection.

## -remarks

If any given bit of <i>Control</i> is set, the corresponding bit from <i>V2</i> is used, otherwise, the
   corresponding bit from <i>V1</i> is used. The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

Result.u[0] = (V1.u[0] & ~Control.u[0]) | (V2.u[0] & Control.u[0]);
Result.u[1] = (V1.u[1] & ~Control.u[1]) | (V2.u[1] & Control.u[1]);
Result.u[2] = (V1.u[2] & ~Control.u[2]) | (V2.u[2] & Control.u[2]);
Result.u[3] = (V1.u[3] & ~Control.u[3]) | (V2.u[3] & Control.u[3]);

return Result;
```


Manual construction of a control vector is not necessary. There are two simple ways of constructing an appropriate
   control vector:

<ul>
<li>
Using the <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselectcontrol">XMVectorSelectControl</a> function to construct a control vector.

See <a href="/windows/win32/api/directxmath/nf-directxmath-xmvectorselectcontrol">Using XMVectorSelect and
       XMVectorSelectControl</a> for a demonstration of how this function can be used.

</li>
<li>
The control vector can be constructed using the XM_SELECT_[0,1] constant (see
       <a href="/windows/desktop/dxmath/ovw-xnamath-reference-constants">DirectXMath Library Constants</a>). As an example, in pseudo-code, an instance of
       <i>Control</i> with the elements:


```
   Control = { XM_SELECT_0,   XM_SELECT_1,   XM_SELECT_0,   XM_SELECT_1 }
```


would return a vector <i>Result</i> with the following components of <i>V1</i> and <i>V2</i>


```
   Result = { V1.X,  V2.Y,   V1.Z,   V2.W }
```


</li>
</ul>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-component-wise">Component-Wise Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorselectcontrol">XMVectorSelectControl</a>
