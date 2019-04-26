---
UID: NF:directxmath.XMMATRIX.operator-mult
title: XMMATRIX::operator-mult
author: windows-sdk-content
description: Performs a matrix multiplication of the current instance of XMMATRIX by another instance of XMMATRIX.
old-location: dxmath\xmmatrix_operator_mul.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMMATRIX.operator *(const XMMATRIX)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMMATRIX.operator *, Use DirectX::::XMMATRIX::operator *, XMMATRIX structure [DirectX Math Support APIs],operator * method, XMMATRIX.operator *, XMMATRIX.operator*, XMMATRIX.operator-mult, XMMATRIX::operator*, XMMATRIX::operator-mult, dxmath.xmmatrix_operator_mul, operator * method [DirectX Math Support APIs], operator * method [DirectX Math Support APIs],XMMATRIX structure, operator*
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMMATRIX.operator *
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMMATRIX::operator-mult


## -description


Performs a matrix multiplication of the current instance of <code>XMMATRIX</code> by another instance of <code>XMMATRIX</code>.

This operator performs a matrix multiplication of the current instance of <a href="https://msdn.microsoft.com/64dd4128-103b-4d54-98f3-cc908170d81c">XMMATRIX</a> by another instance of <code>XMMATRIX</code>.
<div class="alert"><b>Note</b>  This operator is only available when developing with C++.</div><div> </div>

## -parameters




### -param M [ref]

Instance of <code>XMMATRIX</code>  to be multiplied against the current instance of <code>XMMATRIX</code>.


## -returns



An instance of <code>XMMATRIX</code> containing the result of the matrix multiplication.




## -remarks



The current <code>XMMATRIX</code> is the left hand side of the matrix multiplication.  That is  the matrix operation <i>mat2 =  mat1 * M  </i> can be implemented as:
      

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
      XMMATRIX mat1;
      XMMATRIX mat2;
      XMMATRIX M
      mat2 = mat1 * M</pre>
</td>
</tr>
</table></span></div>
And is equivalent to using <a href="https://msdn.microsoft.com/13acd0b4-7fa6-4663-a613-1e63f24aed5f"> and
	 assigning the result to the call's first argument.</a>


<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
      const XMMATRIX&amp; M;
      XMMATRIX&amp; mat1;
      XMMATRIX&amp; mat2;
      mat2 = XMMatrixMultiply(mat1, M);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/64dd4128-103b-4d54-98f3-cc908170d81c">XMMATRIX</a>



<a href="https://msdn.microsoft.com/74deddbd-0472-43fd-8ad6-2e933812eb14">XMMATRIX Operators</a>
 

 

