---
UID: NF:directxmath.XMMATRIX.operator-assign
title: XMMATRIX::operator-assign
description: Assigns the matrix data of one instance of XMMATRIX to the current instance of XMMATRIX and returns a reference to the current instance.
helpviewer_keywords: ["Use DirectX..XMMATRIX.operator =","Use DirectX::::XMMATRIX::operator =","XMMATRIX structure [DirectX Math Support APIs]","operator = method","XMMATRIX.operator =","XMMATRIX.operator-assign","XMMATRIX.operator=","XMMATRIX::operator-assign","XMMATRIX::operator=","dxmath.xmmatrix_operator_eq","operator = method [DirectX Math Support APIs]","operator = method [DirectX Math Support APIs]","XMMATRIX structure","operator="]
old-location: dxmath\xmmatrix_operator_eq.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMMATRIX.operator =(const XMMATRIX)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMATRIX.operator =, Use DirectX::::XMMATRIX::operator =, XMMATRIX structure [DirectX Math Support APIs],operator = method, XMMATRIX.operator =, XMMATRIX.operator-assign, XMMATRIX.operator=, XMMATRIX::operator-assign, XMMATRIX::operator=, dxmath.xmmatrix_operator_eq, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMMATRIX structure, operator=
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
 - XMMATRIX::operator=
 - directxmath/XMMATRIX::operator=
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
 - XMMATRIX.operator =
---

# XMMATRIX::operator-assign


## -description

Assigns the matrix data of one instance of <code>XMMATRIX</code> to the current instance of
	<code>XMMATRIX</code> and returns a <code>reference</code> to the current instance.  


This operator assigns the matrix data of one instance of <a href="/windows/win32/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a> to the current instance of <code>XMMATRIX</code> and returns a <code>reference</code> to the current
	instance.
<div class="alert"><b>Note</b>  This operator is only available when developing with C++.</div><div> </div>

## -parameters

### -param M [ref]

Instance of <code>XMMATRIX</code> whose data
      is used to update the current instance.

## -returns

A <code>reference</code> to the current instance of <code>XMMATRIX</code>, which has been updated by this operator.

## -remarks

The following pseudocode demonstrates the operation of this operator:

<div class="code"><span><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>

   XMMATRIX mat1;
   XMMATRIX M;
   // mat1=mat1*M
   for (int i=0;i&lt;4;i++){
       for (int j=0;j&lt;4;j++){
           mat1.m[i][j]=M.m[i][j];
       }
   }
    </pre>
</td>
</tr>
</table></span></div>

## -see-also

<b>Reference</b>



<a href="/windows/win32/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a>



<a href="/windows/win32/dxmath/ovw-xmmatrix-operators">XMMATRIX Operators</a>
