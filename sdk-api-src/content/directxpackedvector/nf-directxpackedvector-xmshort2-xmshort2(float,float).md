---
UID: NF:directxpackedvector.XMSHORT2.XMSHORT2(float,float)
title: XMSHORT2 function
author: windows-sdk-content
description: Initializes a new instance of XMSHORT2 from two float arguments.
old-location: dxmath\xmshort2_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMSHORT2.#ctor(float,float)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMSHORT2 constructor [DirectX Math Support APIs], XMSHORT2 constructor [DirectX Math Support APIs],XMSHORT2 structure, XMSHORT2 structure [DirectX Math Support APIs],XMSHORT2 constructor, XMSHORT2.XMSHORT2(float,float), dxmath.xmshort2_ctor_4
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
 - XMSHORT2.XMSHORT2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMSHORT2
: 
---

# XMSHORT2 function


## -description


Initializes a new instance of <code>XMSHORT2</code> from two <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/C41BEAA7-E620-4D64-8408-584CDB6F835A">XMSHORT2</a> from two
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMSHORT2</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMSHORT2</code> instance.
		


## -remarks



The magnitude of each argument to the constructor will be clamped to the range supported
	    by an 16-bit signed integer [-32767.0, 32767.0].
	

The following pseudocode demonstrates the operation of this constructor:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMSHORT2 instance;

	instance.x = (int16_t)min( max( _x, -32767.0 ), 32767.0 );
	instance.y = (int16_t)min( max( _y, -32767.0 ), 32767.0 );
    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/C41BEAA7-E620-4D64-8408-584CDB6F835A">XMSHORT2</a>



<a href="https://msdn.microsoft.com/b219497b-cc1f-4c0c-918f-5960321ce636">XMSHORT2 Constructors</a>
 

 

