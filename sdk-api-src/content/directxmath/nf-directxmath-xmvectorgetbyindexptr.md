---
UID: NF:directxmath.XMVectorGetByIndexPtr
title: XMVectorGetByIndexPtr function (directxmath.h)
description: Retrieve, into an instance of a floating-point referenced by pointer, the value of one of the four components of an XMVECTOR Data Type containing floating-point data, referenced by index.
helpviewer_keywords: ["Use DirectX..XMVectorGetByIndexPtr","XMVectorGetByIndexPtr","XMVectorGetByIndexPtr method [DirectX Math Support APIs]","dxmath.xmvectorgetbyindexptr"]
old-location: dxmath\xmvectorgetbyindexptr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.accessors.XMVectorGetByIndexPtr(float@,XMVECTOR,size_t)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorGetByIndexPtr, XMVectorGetByIndexPtr, XMVectorGetByIndexPtr method [DirectX Math Support APIs], dxmath.xmvectorgetbyindexptr
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
 - XMVectorGetByIndexPtr
 - directxmath/XMVectorGetByIndexPtr
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
 - XMVectorGetByIndexPtr
---

# XMVectorGetByIndexPtr function


## -description

Retrieve, into an instance of a floating-point referenced by pointer, the value of one of the four components of an
  <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> containing floating-point data, referenced by index.

## -parameters

### -param f [out]

Pointer to an instance of a floating-point object that will receive the value of the <i>i</i> component of the
        <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> object <code>V</code>.

### -param V

A <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR Data Type</a> containing floating-point data.

### -param i

The index of the component to be retrieved.

## -returns

None.

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



<a href="/previous-versions/windows/desktop/legacy/hh404786(v=vs.85)">XMVectorGetByIndex</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectorsetbyindexptr">XMVectorSetByIndexPtr</a>