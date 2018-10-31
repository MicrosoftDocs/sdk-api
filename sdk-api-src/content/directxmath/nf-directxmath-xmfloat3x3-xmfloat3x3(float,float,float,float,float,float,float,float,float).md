---
UID: NF:directxmath.XMFLOAT3X3.XMFLOAT3X3(float,float,float,float,float,float,float,float,float)
title: XMFLOAT3X3 function
author: windows-sdk-content
description: Initializes a new instance of the XMFLOAT3X3 structure from nine scalar float values.
old-location: dxmath\xmfloat3x3_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3X3.#ctor(float,float,float,float,float,float,float,float,float)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: XMFLOAT3X3 constructor [DirectX Math Support APIs], XMFLOAT3X3 constructor [DirectX Math Support APIs],XMFLOAT3X3 structure, XMFLOAT3X3 structure [DirectX Math Support APIs],XMFLOAT3X3 constructor, XMFLOAT3X3.XMFLOAT3X3(float,float,float,float,float,float,float,float,float), dxmath.xmfloat3x3_ctor_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - XMFLOAT3X3.XMFLOAT3X3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMFLOAT3X3
: 
---

# XMFLOAT3X3 function


## -description


Initializes a new instance of the <code>XMFLOAT3X3</code> structure from nine scalar
	<code>float</code> values.
    

Initializes a new instance of the <a href="https://msdn.microsoft.com/6067d4b2-8609-4172-8228-5e3d43638015">XMFLOAT3X3</a> structure from nine
	scalar <code>float</code> values.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param m00

Value used to initialize the <b>_11</b> member (equivalently the <b>m[0,0]</b>member) of the <code>XMFLOAT3X3</code> structure.
	    


### -param m01

Value used to initialize the <b>_12</b> member (equivalently the
		<b>m[0,1]</b>) of the <code>XMFLOAT3X3</code> structure.
	    


### -param m02

Value used to initialize the <b>_13</b> member (equivalently the
		<b>m[0,2]</b>) of the <code>XMFLOAT3X3</code> structure.
	    


### -param m10

Value used to initialize the <b>_21</b> member (equivalently the
		<b>m[1,0]</b>) of the <code>XMFLOAT3X3</code> structure.
	    


### -param m11

Value used to initialize the <b>_22</b> member (equivalently the
		<b>m[1,1]</b>) of the <code>XMFLOAT3X3</code> structure.
	    


### -param m12

Value used to initialize the <b>_23</b> member (equivalently the
		<b>m[1,2]</b>) of the <code>XMFLOAT3X3</code> structure.
	    


### -param m20

Value used to initialize the <b>_31</b> member (equivalently the
		<b>m[2,0]</b>) of the <code>XMFLOAT3X3</code> structure.
	    


### -param m21

Value used to initialize the <b>_32</b> member (equivalently the
		<b>m[2,1]</b>) of the <code>XMFLOAT3X3</code> structure.
	    


### -param m22

Value used to initialize the <b>_33</b> member (equivalently the
		<b>m[2,2]</b>) of the <code>XMFLOAT3X3</code> structure.
	    


## -remarks



The following two pseudocode examples demonstrate the operation of this constructor:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
   XMFLOAT3X3 mat;
   mat._11 = m00;
   mat._12 = m01;
   mat._13 = m02;
   mat._21 = m10;
   mat._22 = m11;
   mat._23 = m12;
   mat._31 = m20;
   mat._32 = m21;
   mat._33 = m22;
      </pre>
</td>
</tr>
</table></span></div>
Or
      

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
   XMFLOAT3X3 mat;
   mat.m[0,0] = m00;
   mat.m[0,1] = m01;
   mat.m[0,2] = m02;
   mat.m[1,0] = m10;
   mat.m[1,1] = m11;
   mat.m[1,2] = m12;
   mat.m[2,0] = m20;
   mat.m[2,1] = m21;
   mat.m[2,2] = m22;
      </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/6067d4b2-8609-4172-8228-5e3d43638015">XMFLOAT3X3</a>



<a href="https://msdn.microsoft.com/1cfad894-60d4-4258-b3ca-178a2dafafc5">XMFLOAT3X3 Constructors</a>
 

 

