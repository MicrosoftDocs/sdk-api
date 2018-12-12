---
UID: NF:directxpackedvector.XMSHORT2.XMSHORT2(int16_t,int16_t)
title: XMSHORT2::XMSHORT2(int16_t,int16_t)
author: windows-sdk-content
description: Initializes a new instance of XMSHORT2 from two int16_t arguments.
old-location: dxmath\xmshort2_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMSHORT2.#ctor(int16_t,int16_t)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMSHORT2, XMSHORT2 constructor [DirectX Math Support APIs], XMSHORT2 constructor [DirectX Math Support APIs],XMSHORT2 structure, XMSHORT2 structure [DirectX Math Support APIs],XMSHORT2 constructor, XMSHORT2.XMSHORT2, XMSHORT2.XMSHORT2(int16_t,int16_t), XMSHORT2::XMSHORT2, XMSHORT2::XMSHORT2(int16_t,int16_t), dxmath.xmshort2_ctor_2
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
 - XMSHORT2.XMSHORT2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMSHORT2::XMSHORT2(int16_t,int16_t)


## -description


Initializes a new instance of <code>XMSHORT2</code> from two <code>int16_t</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/en-us/library/Ee420195(v=VS.85).aspx">XMSHORT2</a> from two
	<code>int16_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMSHORT2</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMSHORT2</code> instance.
		


## -remarks



The following pseudocode demonstrates the operation of this constructor:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMSHORT2 instance;

	instance.x = _x;
	instance.y = _y;
    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Ee420195(v=VS.85).aspx">XMSHORT2</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415425(v=VS.85).aspx">XMSHORT2 Constructors</a>
 

 

