---
UID: NF:directxpackedvector.XMUSHORTN2.XMUSHORTN2(float,float)
title: XMUSHORTN2::XMUSHORTN2(float,float)
author: windows-sdk-content
description: Initializes a new instance of XMUSHORTN2 from two normalized floatarguments.
old-location: dxmath\xmushortn2_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUSHORTN2.#ctor(float,float)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMUSHORTN2, XMUSHORTN2 constructor [DirectX Math Support APIs], XMUSHORTN2 constructor [DirectX Math Support APIs],XMUSHORTN2 structure, XMUSHORTN2 structure [DirectX Math Support APIs],XMUSHORTN2 constructor, XMUSHORTN2.XMUSHORTN2, XMUSHORTN2.XMUSHORTN2(float,float), XMUSHORTN2::XMUSHORTN2, XMUSHORTN2::XMUSHORTN2(float,float), dxmath.xmushortn2_ctor_4
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
 - XMUSHORTN2.XMUSHORTN2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMUSHORTN2::XMUSHORTN2(float,float)


## -description


Initializes a new instance of <code>XMUSHORTN2</code> from two normalized <code>float</code>arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/05f62462-2b6a-4d1b-bf83-9109a254839e">XMUSHORTN2</a> from two
	normalized <code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

A normalized value for the x-coordinate of the vector.
		

This argument should be between 0.0 and 1.0; during the instantiation of an
		    instance of <code>XMUSHORTN2</code>, it is multiplied by <code>65535.0f</code> and
		    then stored as the <b>x</b> member of the structure.
		


### -param _y

A normalized value for the y-coordinate of the vector, the <b>y</b> of the
		    new instance of <code>XMUSHORTN2</code>.
		

This argument should be between 0.0 and 1.0; during the instantiation of an
		    instance of <code>XMUSHORTN2</code>, it is multiplied by <code>65535.0f</code> and
		    then stored as the <b>y</b> member of the structure.
		


## -remarks



All input values,<i>_x</i> and <i>_y</i> are clamped to a range of 0.0 to 1.0.
	

The following pseudocode demonstrates the operation of this constructor:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMUSHORTN2 instance;
	_x1=min( max( _x, 0.0 ), 1.0 );
	_y1=min( max( _y, 0.0 ), 1.0 );
	_x1 = round( _x1 * 65535.0f);
	_y1 = round( _y1 * 65535.0f);
	instance._x = _x1;
	instance._y = _y1;
	</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/05f62462-2b6a-4d1b-bf83-9109a254839e">XMUSHORTN2</a>



<a href="https://msdn.microsoft.com/89d5f55f-5603-4bc5-bf0b-4d6dae675ca3">XMUSHORTN2 Constructors</a>
 

 

