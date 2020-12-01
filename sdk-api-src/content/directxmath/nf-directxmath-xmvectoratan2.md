---
UID: NF:directxmath.XMVectorATan2
title: XMVectorATan2 function (directxmath.h)
description: Computes the arctangent of Y/X.
helpviewer_keywords: ["Use DirectX..XMVectorATan2","XMVectorATan2","XMVectorATan2 method [DirectX Math Support APIs]","dxmath.xmvectoratan2"]
old-location: dxmath\xmvectoratan2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transcendental.XMVectorATan2(XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVectorATan2, XMVectorATan2, XMVectorATan2 method [DirectX Math Support APIs], dxmath.xmvectoratan2
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
 - XMVectorATan2
 - directxmath/XMVectorATan2
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
 - XMVectorATan2
---

# XMVectorATan2 function


## -description

Computes the arctangent of <i>Y</i>/<i>X</i>.

## -parameters

### -param Y [in]

First vector.

### -param X [in]

Second vector.

## -returns

Returns a vector. Each component is the arctangent of the corresponding <i>Y</i> component divided by the
       corresponding <i>X</i> component. Each component is in the range (-PI/2, PI/2).

<code>XMVectorATan2</code> returns the following values for the specified special input values.

<table>
<tr>
<th>Input Value</th>
<th>Return Value</th>
</tr>
<tr>
<td>Y == 0 and X &lt; 0</td>
<td>Pi with the same sign as Y</td>
</tr>
<tr>
<td>Y == 0 and X &gt; 0</td>
<td>0 with the same sign as Y</td>
</tr>
<tr>
<td>Y != 0 and X == 0</td>
<td>Pi / 2 with the same sign as Y</td>
</tr>
<tr>
<td>X == -Infinity and Y is finite</td>
<td>Pi with the same sign as Y</td>
</tr>
<tr>
<td>X == +Infinity and Y is finite</td>
<td>0 with the same sign as Y</td>
</tr>
<tr>
<td>Y == Infinity and X is finite</td>
<td>Pi / 2 with the same sign as Y</td>
</tr>
<tr>
<td>Y == Infinity and X == -Infinity</td>
<td>3Pi / 4 with the same sign as Y</td>
</tr>
<tr>
<td>Y == Infinity and X == +Infinity</td>
<td>Pi / 4 with the same sign as Y</td>
</tr>
</table>

## -remarks

This function uses a 17-degree minimax approximation.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector-transcendental">Transcendental Vector Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectoratan">XMVectorATan</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectoratan2est">XMVectorATan2Est</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectoratanest">XMVectorATanEst</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvectortan">XMVectorTan</a>