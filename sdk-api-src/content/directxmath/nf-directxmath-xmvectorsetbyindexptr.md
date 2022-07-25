---
UID: NF:directxmath.XMVectorSetByIndexPtr
title: XMVectorSetByIndexPtr function (directxmath.h)
description: Use a pointer to a floating-point instance to set the value of one of the four components of an XMVECTOR Data Type containing floating-point data referenced by an index.
helpviewer_keywords: ["Use DirectX..XMVectorSetByIndexPtr","XMVectorSetByIndexPtr","XMVectorSetByIndexPtr method [DirectX Math Support APIs]","dxmath.xmvectorsetbyindexptr"]
old-location: dxmath\xmvectorsetbyindexptr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.accessors.XMVectorSetByIndexPtr(XMVECTOR,float,size_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorSetByIndexPtr, XMVectorSetByIndexPtr, XMVectorSetByIndexPtr method [DirectX Math Support APIs], dxmath.xmvectorsetbyindexptr
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
 - XMVectorSetByIndexPtr
 - directxmath/XMVectorSetByIndexPtr
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
 - XMVectorSetByIndexPtr
---

# XMVectorSetByIndexPtr function


## -description

Use a pointer to a floating-point instance to set the value of one of the four components of an
  <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> containing floating-point data referenced by an index.

## -parameters

### -param V

A <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> containing floating-point data.

### -param f [in]

A pointer to a floating-point instance used to set the <i>i</i> component of the returned
        <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a>.

### -param i

The index of the component to be set.

## -returns

An instance of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> whose <i>i</i> component has been set to the floating-point value
       provided by the argument <i>f</i>. All other components of the returned <b>XMVECTOR Data Type</b> instance
       have the same value as those of the input vector <i>V</i>.

## -remarks

The value of <i>i</i> must be positive and less than or equal to three ( <i>0 </i> &lt;= <i> i </i> &lt;=
   <i> 3</i> ).

The indexes have the following correspondence with <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> vector components:

<table>
<tr>
<th>Index</th>
<th>Component</th>
</tr>
<tr>
<td>
<code>0</code>

</td>
<td>
<code>x</code>

</td>
</tr>
<tr>
<td>
<code>1</code>

</td>
<td>
<code>y</code>

</td>
</tr>
<tr>
<td>
<code>2</code>

</td>
<td>
<code>z</code>

</td>
</tr>
<tr>
<td>
<code>3</code>

</td>
<td>
<code>w</code>

</td>
</tr>
</table>
 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-accessors">DirectXMath Library Vector Accessor Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorgetbyindexptr">XMVectorGetByIndexPtr</a>



<a href="/previous-versions/windows/desktop/legacy/hh404810(v=vs.85)">XMVectorSetByIndex</a>