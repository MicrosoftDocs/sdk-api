---
UID: NF:directxpackedvector.XMSHORTN4.XMSHORTN4(int16_t,int16_t,int16_t,int16_t)
title: XMSHORTN4::XMSHORTN4(int16_t,int16_t,int16_t,int16_t)
author: windows-sdk-content
description: Initializes a new instance of XMSHORTN4 from four int16_t arguments.
old-location: dxmath\xmshortn4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMSHORTN4.#ctor(int16_t,int16_t,int16_t,int16_t)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMSHORTN4, XMSHORTN4 constructor [DirectX Math Support APIs], XMSHORTN4 constructor [DirectX Math Support APIs],XMSHORTN4 structure, XMSHORTN4 structure [DirectX Math Support APIs],XMSHORTN4 constructor, XMSHORTN4.XMSHORTN4, XMSHORTN4.XMSHORTN4(int16_t,int16_t,int16_t,int16_t), XMSHORTN4::XMSHORTN4, XMSHORTN4::XMSHORTN4(int16_t,int16_t,int16_t,int16_t), dxmath.xmshortn4_ctor_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - XMSHORTN4.XMSHORTN4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMSHORTN4::XMSHORTN4(int16_t,int16_t,int16_t,int16_t)


## -description


Initializes a new instance of <code>XMSHORTN4</code> from four <code>int16_t</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/en-us/library/Ee420216(v=VS.85).aspx">XMSHORTN4</a> from four
	<code>int16_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMSHORTN4</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMSHORTN4</code> instance.
		


### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMSHORTN4</code> instance.
		


### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMSHORTN4</code> instance.
		


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
	XMSHORTN4 instance;

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



<a href="https://msdn.microsoft.com/en-us/library/Ee420216(v=VS.85).aspx">XMSHORTN4</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415434(v=VS.85).aspx">XMSHORTN4 Constructors</a>
 

 

