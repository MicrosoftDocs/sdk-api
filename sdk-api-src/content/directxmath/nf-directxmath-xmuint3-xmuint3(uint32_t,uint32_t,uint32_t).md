---
UID: NF:directxmath.XMUINT3.XMUINT3(uint32_t,uint32_t,uint32_t)
title: XMUINT3 function
author: windows-sdk-content
description: Initializes a new instance of XMUINT3 from three uint32_t arguments.
old-location: dxmath\xmuint3_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUINT3.#ctor(uint32_t,uint32_t,uint32_t)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMUINT3 constructor [DirectX Math Support APIs], XMUINT3 constructor [DirectX Math Support APIs],XMUINT3 structure, XMUINT3 structure [DirectX Math Support APIs],XMUINT3 constructor, XMUINT3.XMUINT3(uint32_t,uint32_t,uint32_t), dxmath.xmuint3_ctor_2
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
 - XMUINT3.XMUINT3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMUINT3
: 
---

# XMUINT3 function


## -description


Initializes a new instance of <code>XMUINT3</code> from three <code>uint32_t</code> arguments.

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/B3B7CD31-8759-4674-AAA9-E13DA1D67675">XMUINT3</a> from three <code>uint32_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters




### -param _x

Value to be stored in the x-component (the <b>x</b> member) of the new instance of
	    <code>XMUINT3</code>.
	


### -param _y

Value to be stored in the y-component (the <b>y</b> member) of the new instance of
	    <code>XMUINT3</code>.
	


### -param _z

Value to be stored in the z-component (the <b>z</b> member) of the new instance of
	    <code>XMUINT3</code>.
	


## -remarks



The following pseudocode demonstrates the operation of this constructor:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMUINT3 instance;
	instance.x =  _x;
	instance.y =  _y;
	instance.z =  _z;
    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/B3B7CD31-8759-4674-AAA9-E13DA1D67675">XMUINT3</a>



<a href="https://msdn.microsoft.com/f3737cb1-36a0-4dbc-94d5-237e7395670e">XMUINT3 Constructors</a>
 

 

