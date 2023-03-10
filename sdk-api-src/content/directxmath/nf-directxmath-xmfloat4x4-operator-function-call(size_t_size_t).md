---
UID: NF:directxmath.XMFLOAT4X4.operator-function-call(size_t,size_t)
title: XMFLOAT4X4::operator-function-call(size_t,size_t)
description: Returns a reference to a matrix element of an instance XMFLOAT4X4 as specified by row and column arguments.
helpviewer_keywords: ["XMFLOAT4X4 structure [DirectX Math Support APIs]","operator () method","XMFLOAT4X4.operator ()(size_t","size_t)","XMFLOAT4X4.operator (size_t","size_t)","XMFLOAT4X4.operator()","XMFLOAT4X4.operator-function-call(size_t","size_t)","XMFLOAT4X4::operator()","XMFLOAT4X4::operator-function-call(size_t","size_t)","dxmath.xmfloat4x4_operator_parens_1","operator () method [DirectX Math Support APIs]","operator () method [DirectX Math Support APIs]","XMFLOAT4X4 structure","operator()"]
old-location: dxmath\xmfloat4x4_operator_parens_1.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT4X4.operator ()(size_t,size_t)
ms.date: 12/05/2018
ms.keywords: XMFLOAT4X4 structure [DirectX Math Support APIs],operator () method, XMFLOAT4X4.operator ()(size_t,size_t), XMFLOAT4X4.operator (size_t,size_t), XMFLOAT4X4.operator(), XMFLOAT4X4.operator-function-call(size_t,size_t), XMFLOAT4X4::operator(), XMFLOAT4X4::operator-function-call(size_t,size_t), dxmath.xmfloat4x4_operator_parens_1, operator () method [DirectX Math Support APIs], operator () method [DirectX Math Support APIs],XMFLOAT4X4 structure, operator()
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
 - XMFLOAT4X4::operator()
 - directxmath/XMFLOAT4X4::operator()
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
 - XMFLOAT4X4.operator ()
---

# XMFLOAT4X4::operator-function-call(size_t,size_t)


## -description

Returns a <code>reference</code> to a matrix element of an instance <code>XMFLOAT4X4</code> as specified by row and column
  arguments.
<div class="alert"><b>Note</b>  This operator is only available under C++.</div><div> </div>

## -parameters

### -param Row

Row containing the matrix element of interest. Row specification is 0 based.

### -param Column

Column containing the matrix element of interest. Column specification is 0 based.

## -returns

A <code>reference</code> to the matrix element specified by the operator's <b>Row</b> and <b>Column</b> arguments.

## -remarks

As a <code>reference</code> to the matrix element is returned, this operator can be used to update the value of an element
   of an instance of <code>XMFLOAT4X4</code>.

The following example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
     XMFLOAT4X4 mat;
     float&amp; a= mat(2,3);
     a=42.0;
    </pre>
</td>
</tr>
</table></span></div>
will set the value of the <i>mat.m[2,3]</i> (or equivalently mat._34) to 42.0.

## -see-also

<b>Reference</b>



<a href="/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4">XMFLOAT4X4</a>



<a href="/windows/win32/dxmath/ovw-xmfloat4x4-operators">XMFLOAT4X4 Operators</a>
