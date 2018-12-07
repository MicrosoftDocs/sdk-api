---
UID: NF:directxmath.XMFLOAT4A.XMFLOAT4A(const float)
title: XMFLOAT4A function
author: windows-sdk-content
description: Initializes a new instance of XMFLOAT4 from a four element float array argument.
old-location: dxmath\xmfloat4_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT4.#ctor(const float)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: XMFLOAT4 constructor [DirectX Math Support APIs], XMFLOAT4 constructor [DirectX Math Support APIs],XMFLOAT4 structure, XMFLOAT4 structure [DirectX Math Support APIs],XMFLOAT4 constructor, XMFLOAT4.XMFLOAT4(const float*), XMFLOAT4A.XMFLOAT4A(const float), dxmath.xmfloat4_ctor_3
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
 - XMFLOAT4.XMFLOAT4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMFLOAT4A
: 
---

# XMFLOAT4A function


## -description


Initializes a new instance of <code>XMFLOAT4</code> from a four element <code>float</code> array
	argument.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/2af4929b-9e44-4229-916e-d7d8eae07306">XMFLOAT4</a> from a from
	a four element <code>float</code> array argument.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param pArray

Four element <code>float</code> array containing the values used to initialize the
		    four components of a new instance of <code>XMFLOAT4</code>.
		


## -remarks



The following pseudocode demonstrates the operation of this constructor:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
	XMFLOAT4 instance;
	instance.x = pArray[0];
	instance.y = pArray[1];
	instance.z = pArray[2];
	instance.w = pArray[3];

    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/2af4929b-9e44-4229-916e-d7d8eae07306">XMFLOAT4</a>



<a href="https://msdn.microsoft.com/e52801d1-d363-436b-8be0-ae7a173db75c">XMFLOAT4 Constructors</a>
 

 

