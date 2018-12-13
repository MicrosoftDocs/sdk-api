---
UID: NF:directxpackedvector.XMSHORTN2.XMSHORTN2(float,float)
title: XMSHORTN2::XMSHORTN2(float,float)
author: windows-sdk-content
description: Initializes a new instance of XMSHORTN2 from two normalized floatarguments.
old-location: dxmath\xmshortn2_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMSHORTN2.#ctor(float,float)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMSHORTN2, XMSHORTN2 constructor [DirectX Math Support APIs], XMSHORTN2 constructor [DirectX Math Support APIs],XMSHORTN2 structure, XMSHORTN2 structure [DirectX Math Support APIs],XMSHORTN2 constructor, XMSHORTN2.XMSHORTN2, XMSHORTN2.XMSHORTN2(float,float), XMSHORTN2::XMSHORTN2, XMSHORTN2::XMSHORTN2(float,float), dxmath.xmshortn2_ctor_4
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
 - XMSHORTN2.XMSHORTN2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMSHORTN2::XMSHORTN2(float,float)


## -description


Initializes a new instance of <code>XMSHORTN2</code> from two normalized <code>float</code>arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/DAE0ABD5-D2FD-40ED-8F0B-27A42C93508C">XMSHORTN2</a> from two
	normalized <code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

A normalized value for the x-coordinate of the vector.
		

This argument should be between -1.0 and 1.0; during the instantiation of an
		    instance of <code>XMSHORTN2</code>, it is multiplied by <code>32767.0f</code> and
		    then stored as the <b>x</b> member of the structure.
		


### -param _y

A normalized value for the y-coordinate of the vector, the <b>y</b> of the
		    new instance of <code>XMSHORTN2</code>.
		

This argument should be between -1.0 and 1.0; during the instantiation of an
		    instance of <code>XMSHORTN2</code>, it is multiplied by <code>32767.0f</code> and
		    then stored as the <b>y</b> member of the structure.
		


## -remarks



All input values,<i>_x</i> and <i>_y</i> are clamped to a range of -1.0 to 1.0.
	

The following pseudocode demonstrates the operation of this constructor:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMSHORTN2 instance;
	_x1=min( max( _x, -1.0 ), 1.0 );
	_y1=min( max( _y, -1.0 ), 1.0 );
	_x1 = round( _x1 * 32767.0f);
	_y1 = round( _y1 * 32767.0f);
	instance._x = _x1;
	instance._y = _y1;
	</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/DAE0ABD5-D2FD-40ED-8F0B-27A42C93508C">XMSHORTN2</a>



<a href="https://msdn.microsoft.com/3a9ee31d-7ab7-4600-ac21-b10225ac28c2">XMSHORTN2 Constructors</a>
 

 

