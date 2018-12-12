---
UID: NF:directxpackedvector.XMUBYTEN2.XMUBYTEN2(uint8_t,uint8_t)
title: XMUBYTEN2::XMUBYTEN2(uint8_t,uint8_t)
author: windows-sdk-content
description: Initializes a new instance of XMUBYTEN2 from two uint8_t arguments.
old-location: dxmath\xmubyten2_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUBYTEN2.#ctor(uint8_t,uint8_t)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMUBYTEN2, XMUBYTEN2 constructor [DirectX Math Support APIs], XMUBYTEN2 constructor [DirectX Math Support APIs],XMUBYTEN2 structure, XMUBYTEN2 structure [DirectX Math Support APIs],XMUBYTEN2 constructor, XMUBYTEN2.XMUBYTEN2, XMUBYTEN2.XMUBYTEN2(uint8_t,uint8_t), XMUBYTEN2::XMUBYTEN2, XMUBYTEN2::XMUBYTEN2(uint8_t,uint8_t), dxmath.xmubyten2_ctor_3
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
 - XMUBYTEN2.XMUBYTEN2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMUBYTEN2::XMUBYTEN2(uint8_t,uint8_t)


## -description


Initializes a new instance of <code>XMUBYTEN2</code> from two <code>uint8_t</code> arguments.

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/en-us/library/Hh404729(v=VS.85).aspx">XMUBYTEN2 </a> from two <code>uint8_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available with C++.</div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new <code>XMUBYTEN2</code> instance.


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new <code>XMUBYTEN2</code> instance.


## -remarks



Input values are not normalized. The following pseudocode demonstrates the operation of this constructor:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	    XMUBYTEN2 instance;

	    instance.x = _x; 
	    instance.y = _y; 
	</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Hh404729(v=VS.85).aspx">XMUBYTEN2</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449528(v=VS.85).aspx">XMUBYTEN2 Constructors</a>
 

 

