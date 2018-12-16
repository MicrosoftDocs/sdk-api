---
UID: NF:directxmath.XMFLOAT3.XMFLOAT3(float,float,float)
title: XMFLOAT3::XMFLOAT3(float,float,float)
author: windows-sdk-content
description: Initializes a new instance of XMFLOAT3 from three float arguments.
old-location: dxmath\xmfloat3_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3.#ctor(float,float,float)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMFLOAT3, XMFLOAT3 constructor [DirectX Math Support APIs], XMFLOAT3 constructor [DirectX Math Support APIs],XMFLOAT3 structure, XMFLOAT3 structure [DirectX Math Support APIs],XMFLOAT3 constructor, XMFLOAT3.XMFLOAT3, XMFLOAT3.XMFLOAT3(float,float,float), XMFLOAT3::XMFLOAT3, XMFLOAT3::XMFLOAT3(float,float,float), dxmath.xmfloat3_ctor_2
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
 - XMFLOAT3.XMFLOAT3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMFLOAT3::XMFLOAT3(float,float,float)


## -description


Initializes a new instance of <code>XMFLOAT3</code> from three <code>float</code> arguments.

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/en-us/library/Ee419475(v=VS.85).aspx">XMFLOAT3</a> from a three <code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters




### -param _x

Value to be stored in the x-component (the <b>x</b> member) of the new instance of
	    <code>XMFLOAT3</code>.
	


### -param _y

Value to be stored in the y-component (the <b>y</b> member) of the new instance of
	    <code>XMFLOAT3</code>.
	


### -param _z

Value to be stored in the z-component (the <b>z</b> member) of the new instance of
	    <code>XMFLOAT3</code>.
	


## -remarks



The following pseudocode demonstrates the operation of this constructor:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMFLOAT3 instance;
	instance.x =  _x;
	instance.y =  _y;
	instance.z =  _z;
    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Ee419475(v=VS.85).aspx">XMFLOAT3</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415292(v=VS.85).aspx">XMFLOAT3 Constructors</a>
 

 

