---
UID: NF:directxpackedvector.XMSHORTN2.XMSHORTN2(int16_t,int16_t)
title: XMSHORTN2 function
author: windows-sdk-content
description: Initializes a new instance of XMSHORTN2 from two int16_t arguments.
old-location: dxmath\xmshortn2_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMSHORTN2.#ctor(int16_t,int16_t)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: XMSHORTN2 constructor [DirectX Math Support APIs], XMSHORTN2 constructor [DirectX Math Support APIs],XMSHORTN2 structure, XMSHORTN2 structure [DirectX Math Support APIs],XMSHORTN2 constructor, XMSHORTN2.XMSHORTN2(int16_t,int16_t), dxmath.xmshortn2_ctor_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: directxpackedvector.h
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
req.namespace: DirectX::PackedVector
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
 - DirectXPackedVector.h
api_name:
 - XMSHORTN2.XMSHORTN2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMSHORTN2
: 
---

# XMSHORTN2 function


## -description


Initializes a new instance of <code>XMSHORTN2</code> from two <code>int16_t</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/DAE0ABD5-D2FD-40ED-8F0B-27A42C93508C">XMSHORTN2</a> from two
	<code>int16_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMSHORTN2</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMSHORTN2</code> instance.
		


## -remarks



Input values are not normalized. The following pseudocode demonstrates the operation of
	    this constructor:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMSHORTN2 instance;

	instance.x = _x;
	instance.y = _y;


    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/DAE0ABD5-D2FD-40ED-8F0B-27A42C93508C">XMSHORTN2</a>



<a href="https://msdn.microsoft.com/3a9ee31d-7ab7-4600-ac21-b10225ac28c2">XMSHORTN2 Constructors</a>
 

 

