---
UID: NF:directxmath.XMMATRIX.operator-mult-assign
title: XMMATRIX::operator-mult-assign
description: Performs a matrix multiplication of the current instance of XMMATRIX by another instance of XMMATRIX and returns a reference to the current instance, which has been updated.
helpviewer_keywords: ["Use DirectX..XMMATRIX.operator *=","Use DirectX::::XMMATRIX::operator *=","XMMATRIX structure [DirectX Math Support APIs]","operator *= method","XMMATRIX.operator *=","XMMATRIX.operator*=","XMMATRIX.operator-mult-assign","XMMATRIX::operator*=","XMMATRIX::operator-mult-assign","dxmath.xmmatrix_operator_muleq","operator *= method [DirectX Math Support APIs]","operator *= method [DirectX Math Support APIs]","XMMATRIX structure","operator*="]
old-location: dxmath\xmmatrix_operator_muleq.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMMATRIX.operator *=(const XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMATRIX.operator *=, Use DirectX::::XMMATRIX::operator *=, XMMATRIX structure [DirectX Math Support APIs],operator *= method, XMMATRIX.operator *=, XMMATRIX.operator*=, XMMATRIX.operator-mult-assign, XMMATRIX::operator*=, XMMATRIX::operator-mult-assign, dxmath.xmmatrix_operator_muleq, operator *= method [DirectX Math Support APIs], operator *= method [DirectX Math Support APIs],XMMATRIX structure, operator*=
req.header: directxmath.h
req.include-header:
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
f1_keywords:
 - XMMATRIX::operator*=
 - directxmath/XMMATRIX::operator*=
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMMATRIX.operator *=
---

# XMMATRIX::operator-mult-assign


## -description

Performs a matrix multiplication of the current instance of <code>XMMATRIX</code> by another instance of <code>XMMATRIX</code> and returns a reference to the current instance, which has been updated.

This operator performs a matrix multiplication of the current instance of <a href="/windows/win32/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a> by another instance of <code>XMMATRIX</code> and returns a reference to the current instance, which has been updated.
<div class="alert"><b>Note</b>  This operator is only available when developing with C++.</div><div> </div>

## -parameters

### -param M [ref]

Instance of <code>XMMATRIX</code>  to be multiplied against the current instance of <code>XMMATRIX</code>.

## -returns

Reference to the current instance of <code>XMMATRIX</code>, which has been updated by this operator.

## -remarks

The current <code>XMMATRIX</code> is the left hand side of the matrix multiplication.  That is  the matrix operation <i>mat1 =  mat1 * M  </i> can be implemented as:


<div class="code"><span><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
      XMMATRIX mat1;
      XMMATRIX M
      mat1 *= M</pre>
</td>
</tr>
</table></span></div>
And is equivalent to using operator* and
	 assigning the result to the call's first argument.</a>


<div class="code"><span><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
      const XMMATRIX&amp; M;
      XMMATRIX&amp; mat1;
      mat1 = XMMatrixMultiply(mat1, M);</pre>
</td>
</tr>
</table></span></div>

## -see-also

<b>Reference</b>



<a href="/windows/win32/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a>



<a href="/windows/win32/dxmath/ovw-xmmatrix-operators">XMMATRIX Operators</a>
