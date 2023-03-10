---
UID: NF:directxpackedvector.XMFLOAT3SE.XMFLOAT3SE(uint32_t)
title: XMFLOAT3SE::XMFLOAT3SE(uint32_t) (directxpackedvector.h)
description: Initializes a new instance of XMFLOAT3SE from a uint32_tvariable containing component data in a packed format.
helpviewer_keywords: ["XMFLOAT3SE","XMFLOAT3SE constructor [DirectX Math Support APIs]","XMFLOAT3SE constructor [DirectX Math Support APIs]","XMFLOAT3SE structure","XMFLOAT3SE structure [DirectX Math Support APIs]","XMFLOAT3SE constructor","XMFLOAT3SE.XMFLOAT3SE","XMFLOAT3SE.XMFLOAT3SE(uint32_t)","XMFLOAT3SE::XMFLOAT3SE","XMFLOAT3SE::XMFLOAT3SE(uint32_t)","dxmath.xmfloat3se_ctor_3"]
old-location: dxmath\xmfloat3se_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3SE.#ctor(uint32_t)
ms.date: 12/05/2018
ms.keywords: XMFLOAT3SE, XMFLOAT3SE constructor [DirectX Math Support APIs], XMFLOAT3SE constructor [DirectX Math Support APIs],XMFLOAT3SE structure, XMFLOAT3SE structure [DirectX Math Support APIs],XMFLOAT3SE constructor, XMFLOAT3SE.XMFLOAT3SE, XMFLOAT3SE.XMFLOAT3SE(uint32_t), XMFLOAT3SE::XMFLOAT3SE, XMFLOAT3SE::XMFLOAT3SE(uint32_t), dxmath.xmfloat3se_ctor_3
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XMFLOAT3SE::XMFLOAT3SE
 - directxpackedvector/XMFLOAT3SE::XMFLOAT3SE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXPackedVector.h
api_name:
 - XMFLOAT3SE.XMFLOAT3SE
---

# XMFLOAT3SE::XMFLOAT3SE(uint32_t)


## -description

Initializes a new instance of <code>XMFLOAT3SE</code> from a <code>uint32_t</code> variable  containing component data in a packed format.

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3se">XMFLOAT3SE</a> from a
  <code>uint32_t</code> variable  containing component data in a packed format.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters

### -param Packed

The values of three vector components in a packed format.

## -remarks

The values of the three components of the new instance of <code>XMFLOAT3SE</code> are stored
	in the argument <b>Packed</b> with  the exponent shared by all the mantissas of the floating point values
	of all three components (the <b>e</b> of the <code>XMFLOAT3SE</code> structure) stored in
	the highest order bits, and the mantissa of the x component stored in the least
	significant bits.
 


```

   (E5Z9Y9X9): [32] EEEEEzzz zzzzzzyy yyyyyyyx xxxxxxxx [0]

```


Or in detail:


<ul>
<li>
Bits 0-8 of <b>Packed</b> are the 9 bit <i>mantissa</i> of the
	       <b>x</b> component's floating point value: the <b>xm</b> member of the
	       structure to be instantiated.
	    

</li>
<li>
Bits 9-17 of <b>Packed</b> are the 9 bit <i>mantissa</i> of the
	       <b>y</b> component's floating point value: the <b>ym</b> member of the
	       structure to be instantiated.
	    

</li>
<li>
Bits 18-26 of <b>Packed</b> are the 9 bit <i>mantissa</i> of the
	       <b>z</b> component's floating point value: the <b>zm</b> member of the
	       structure to be instantiated.
	    

</li>
<li>
Bits 27-31 of <b>Packed</b> are the 5 bit <i>exponent</i> used
		with the stored mantissas (<b>xm</b>, <b>ym</b>, <b>zm</b>) to represent
		the size of each component: the <b>e</b> member of the structure to be
		instantiated.
	    

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3se">XMFLOAT3SE</a>



<a href="/windows/desktop/dxmath/xmfloat3se-ctor">XMFLOAT3SE Constructors</a>