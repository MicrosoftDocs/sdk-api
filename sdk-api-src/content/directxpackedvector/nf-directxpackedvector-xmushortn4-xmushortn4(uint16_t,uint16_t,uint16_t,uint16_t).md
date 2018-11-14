---
UID: NF:directxpackedvector.XMUSHORTN4.XMUSHORTN4(uint16_t,uint16_t,uint16_t,uint16_t)
title: XMUSHORTN4 function
author: windows-sdk-content
description: Initializes a new instance of XMUSHORTN4 from four uint16_t arguments.
old-location: dxmath\xmushortn4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUSHORTN4.#ctor(uint16_t,uint16_t,uint16_t,uint16_t)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMUSHORTN4 constructor [DirectX Math Support APIs], XMUSHORTN4 constructor [DirectX Math Support APIs],XMUSHORTN4 structure, XMUSHORTN4 structure [DirectX Math Support APIs],XMUSHORTN4 constructor, XMUSHORTN4.XMUSHORTN4(uint16_t,uint16_t,uint16_t,uint16_t), dxmath.xmushortn4_ctor_2
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
 - XMUSHORTN4.XMUSHORTN4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMUSHORTN4
: 
---

# XMUSHORTN4 function


## -description


Initializes a new instance of <code>XMUSHORTN4</code> from four <code>uint16_t</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/bd514dcf-2b94-411e-b47c-aad3b972754a">XMUSHORTN4</a> from four
	<code>uint16_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMUSHORTN4</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMUSHORTN4</code> instance.
		


### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMUSHORTN4</code> instance.
		


### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMUSHORTN4</code> instance.
		


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
	XMUSHORTN4 instance;

	instance.x = _x;
	instance.y = _y;
	instance.z = _z;
	instance.w = _w;

    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/bd514dcf-2b94-411e-b47c-aad3b972754a">XMUSHORTN4</a>



<a href="https://msdn.microsoft.com/2afe394c-0b3a-470f-a420-5d1c7ee9122e">XMUSHORTN4 Constructors</a>
 

 

