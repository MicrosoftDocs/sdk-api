---
UID: NF:directxpackedvector.XMFLOAT3PK.XMFLOAT3PK(uint32_t)
title: XMFLOAT3PK::XMFLOAT3PK(uint32_t) (directxpackedvector.h)
description: Initializes a new instance of XMFLOAT3PK from a uint32_tvariable containing component data in a packed format.
helpviewer_keywords: ["XMFLOAT3PK","XMFLOAT3PK constructor [DirectX Math Support APIs]","XMFLOAT3PK constructor [DirectX Math Support APIs]","XMFLOAT3PK structure","XMFLOAT3PK structure [DirectX Math Support APIs]","XMFLOAT3PK constructor","XMFLOAT3PK.XMFLOAT3PK","XMFLOAT3PK.XMFLOAT3PK(uint32_t)","XMFLOAT3PK::XMFLOAT3PK","XMFLOAT3PK::XMFLOAT3PK(uint32_t)","dxmath.xmfloat3pk_ctor_3"]
old-location: dxmath\xmfloat3pk_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3PK.#ctor(uint32_t)
ms.date: 12/05/2018
ms.keywords: XMFLOAT3PK, XMFLOAT3PK constructor [DirectX Math Support APIs], XMFLOAT3PK constructor [DirectX Math Support APIs],XMFLOAT3PK structure, XMFLOAT3PK structure [DirectX Math Support APIs],XMFLOAT3PK constructor, XMFLOAT3PK.XMFLOAT3PK, XMFLOAT3PK.XMFLOAT3PK(uint32_t), XMFLOAT3PK::XMFLOAT3PK, XMFLOAT3PK::XMFLOAT3PK(uint32_t), dxmath.xmfloat3pk_ctor_3
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
 - XMFLOAT3PK::XMFLOAT3PK
 - directxpackedvector/XMFLOAT3PK::XMFLOAT3PK
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
 - XMFLOAT3PK.XMFLOAT3PK
---

# XMFLOAT3PK::XMFLOAT3PK(uint32_t)


## -description

Initializes a new instance of <code>XMFLOAT3PK</code> from a <code>uint32_t</code> variable  containing component data in a packed format.

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a> from a
  <code>uint32_t</code> variable  containing component data in a packed format.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters

### -param Packed

The values of three vector components in a packed format.

## -remarks

The values of the three components of the new instance of <code>XMFLOAT3PK</code> are stored
	in the argument <b>Packed</b> with the z component (as a reduced precision
	floating point number) in the most significant bits, and the x component is stored in the
	least significant bits:
 


```

  (Z10Y11X11): [32] ZZZZZzzz zzYYYYYy yyyyXXX XXxxxxxx [0]

```


Or in detail:


<ul>
<li>
Bits 0-5 of <b>v</b> are the 6 bit <i>mantissa</i> of the
	       <b>x</b> component's floating point value: the <b>xm</b> member of new instance of the structure.
	    

</li>
<li>
Bits 6-10 of <b>v</b> are the 5 bit <i>exponent</i> of the
		<b>x</b> component's floating point value the <b>xe</b> member of new instance of the structure.
	    

</li>
<li>
Bits 11-16 of <b>v</b> are the 6-bit <i>mantissa</i> of the
	       <b>y</b> component's floating point value: the <b>ym</b> member of new instance of the structure.
	    

</li>
<li>
Bits 17-21 of <b>v</b> are the 5 bit <i>exponent</i> of the
		<b>y</b> component's floating point value: the <b>ye</b> member of new instance of the structure.
	    

</li>
<li>
Bits 22-26 of <b>v</b> are the 5 bit <i>mantissa</i> of the
	       <b>z</b> component's floating point value: the <b>zm</b> member of new instance of the structure.
	    

</li>
<li>
Bits 27-31 of <b>v</b> are the 5 bit <i>exponent</i> of the
		<b>z</b> component's floating point value: the <b>ze</b> member of new instance of the structure.
	    

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a>



<a href="/windows/desktop/dxmath/xmfloat3pk-ctor">XMFLOAT3PK Constructors</a>