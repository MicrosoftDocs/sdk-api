---
UID: NF:directxmath.XMMATRIX.operator-function-call(size_t,size_t)
title: XMMATRIX::operator-function-call(size_t,size_t)
description: Returns a reference to a matrix element of an instance XMMATRIX as specified by row and column arguments.
helpviewer_keywords: ["XMMATRIX structure [DirectX Math Support APIs]","operator () method","XMMATRIX.operator ()(size_t","size_t)","XMMATRIX.operator (size_t","size_t)","XMMATRIX.operator()","XMMATRIX.operator-function-call(size_t","size_t)","XMMATRIX::operator()","XMMATRIX::operator-function-call(size_t","size_t)","dxmath.xmmatrix_operator_parens_1","operator () method [DirectX Math Support APIs]","operator () method [DirectX Math Support APIs]","XMMATRIX structure","operator()"]
old-location: dxmath\xmmatrix_operator_parens_1.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMMATRIX.operator ()(size_t,size_t)
ms.date: 12/05/2018
ms.keywords: XMMATRIX structure [DirectX Math Support APIs],operator () method, XMMATRIX.operator ()(size_t,size_t), XMMATRIX.operator (size_t,size_t), XMMATRIX.operator(), XMMATRIX.operator-function-call(size_t,size_t), XMMATRIX::operator(), XMMATRIX::operator-function-call(size_t,size_t), dxmath.xmmatrix_operator_parens_1, operator () method [DirectX Math Support APIs], operator () method [DirectX Math Support APIs],XMMATRIX structure, operator()
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
 - XMMATRIX::operator()
 - directxmath/XMMATRIX::operator()
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
 - XMMATRIX.operator ()
---

# XMMATRIX::operator-function-call(size_t,size_t)


## -description

Returns a <code>reference</code> to a matrix element of an instance <code>XMMATRIX</code> as specified by row and column
  arguments.

This operator returns a <code>reference</code> to a matrix element of an instance <a href="/windows/win32/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a> as
  specified by row and column arguments.
<div class="alert"><b>Note</b>  This operator is only available when developing with C++.</div><div> </div>

## -parameters

### -param Row

Row containing the matrix element of interest. Row specification is 0 based.

### -param Column

Column containing the matrix element of interest. Column specification is 0 based.

## -returns

A <code>reference</code> to the matrix element specified by the operator's <b>Row</b> and <b>Column</b> arguments.

## -remarks

This operator is only available when building with ``_XM_NO_INTRINSICS_``.

As a <code>reference</code> to the matrix element is returned, this operator can be used to update the value of an element
   of an instance of <code>XMMATRIX</code>.

The following example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
     XMMATRIX mat;
     float&amp; a= mat(1,2);
     a=42.0;
    </pre>
</td>
</tr>
</table></span></div>
will set the value of the <i>mat.m[1][2]</i> to 42.0.

## -see-also

<b>Reference</b>



<a href="/windows/win32/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a>



<a href="/windows/win32/dxmath/ovw-xmmatrix-operators">XMMATRIX Operators</a>
