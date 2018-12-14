---
UID: NF:directxpackedvector.XMHALF2.XMHALF2(float,float)
title: XMHALF2::XMHALF2(float,float)
author: windows-sdk-content
description: Initializes a new instance of XMHALF2 from two float arguments.
old-location: dxmath\xmhalf2_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMHALF2.#ctor(float,float)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMHALF2, XMHALF2 constructor [DirectX Math Support APIs], XMHALF2 constructor [DirectX Math Support APIs],XMHALF2 structure, XMHALF2 structure [DirectX Math Support APIs],XMHALF2 constructor, XMHALF2.XMHALF2, XMHALF2.XMHALF2(float,float), XMHALF2::XMHALF2, XMHALF2::XMHALF2(float,float), dxmath.xmhalf2_ctor_4
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
 - XMHALF2.XMHALF2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMHALF2::XMHALF2(float,float)


## -description


Initializes a new instance of <code>XMHALF2</code> from two <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/en-us/library/Ee419652(v=VS.85).aspx">XMHALF2</a> from two
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMHALF2</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMHALF2</code> instance.
		


## -remarks



If the magnitude of one of this constructor's floating point arguments cannot be
	    represented by the <code>HALF</code> type, the corresponding member of the new instance of
	    <code>XMHALF2</code> will be infinity for a 16-bit integer (+0x7FFF).
	

The following pseudocode demonstrates the operation of this constructor using the XNA
	    Math <a href="https://msdn.microsoft.com/463abe18-b8c4-44be-9740-b7e0459d3ebd">XMConvertFloatToHalf</a> function:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMHALF2 instance;

	instance.x = XMConvertFloatToHalf(_x);
	instance.y = XMConvertFloatToHalf(_y);
    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Ee419652(v=VS.85).aspx">XMHALF2</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415315(v=VS.85).aspx">XMHALF2 Constructors</a>
 

 

