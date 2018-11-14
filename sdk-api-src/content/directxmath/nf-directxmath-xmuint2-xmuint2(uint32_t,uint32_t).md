---
UID: NF:directxmath.XMUINT2.XMUINT2(uint32_t,uint32_t)
title: XMUINT2 function
author: windows-sdk-content
description: Initializes a new instance of XMUINT2 from two uint32_t arguments.
old-location: dxmath\xmuint2_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUINT2.#ctor(uint32_t,uint32_t)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: XMUINT2 constructor [DirectX Math Support APIs], XMUINT2 constructor [DirectX Math Support APIs],XMUINT2 structure, XMUINT2 structure [DirectX Math Support APIs],XMUINT2 constructor, XMUINT2.XMUINT2(uint32_t,uint32_t), dxmath.xmuint2_ctor_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: directxmath.h
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
req.namespace: Use DirectX.
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
 - DirectXMath.h
api_name:
 - XMUINT2.XMUINT2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMUINT2
: 
---

# XMUINT2 function


## -description


Initializes a new instance of <code>XMUINT2</code> from two <code>uint32_t</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/33240440-20A8-4320-AF2F-40BA287CB107">XMUINT2</a> from two
	<code>uint32_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMUINT2</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMUINT2</code> instance.
		


## -remarks



The following pseudocode demonstrates the operation of this constructor:
	

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMUINT2 instance;

	instance.x = _x;
	instance.y = _y;

    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/33240440-20A8-4320-AF2F-40BA287CB107">XMUINT2</a>



<a href="https://msdn.microsoft.com/296d8eb0-a39f-494e-8524-5bf360dd1160">XMUINT2 Constructors</a>
 

 

