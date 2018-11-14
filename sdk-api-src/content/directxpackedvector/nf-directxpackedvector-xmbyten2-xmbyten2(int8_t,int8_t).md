---
UID: NF:directxpackedvector.XMBYTEN2.XMBYTEN2(int8_t,int8_t)
title: XMBYTEN2 function
author: windows-sdk-content
description: Initializes a new instance of XMBYTEN2 from two int8_t arguments.
old-location: dxmath\xmbyten2_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMBYTEN2.#ctor(int8_t,int8_t)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMBYTEN2 constructor [DirectX Math Support APIs], XMBYTEN2 constructor [DirectX Math Support APIs],XMBYTEN2 structure, XMBYTEN2 structure [DirectX Math Support APIs],XMBYTEN2 constructor, XMBYTEN2.XMBYTEN2(int8_t,int8_t), dxmath.xmbyten2_ctor_3
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
 - XMBYTEN2.XMBYTEN2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMBYTEN2
: 
---

# XMBYTEN2 function


## -description


Initializes a new instance of <code>XMBYTEN2</code> from two <code>int8_t</code> arguments.

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/87cadfb8-6b3c-4c66-88c1-c3751edeb3f2">XMBYTEN2 </a> from two <code>int8_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available with C++.</div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new <code>XMBYTEN2</code> instance.


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new <code>XMBYTEN2</code> instance.


## -remarks



Input values are not normalized. The following pseudocode demonstrates the operation of this constructor:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	    XMBYTEN2 instance;

	    instance.x = _x; 
	    instance.y = _y; 
	</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/87cadfb8-6b3c-4c66-88c1-c3751edeb3f2">XMBYTEN2</a>



<a href="https://msdn.microsoft.com/76a96981-e298-41b2-8220-3f7b985fe751">XMBYTEN2 Constructors</a>
 

 

