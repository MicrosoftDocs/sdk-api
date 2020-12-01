---
UID: NF:directxpackedvector.XMBYTEN2.XMBYTEN2(int8_t,int8_t)
title: XMBYTEN2::XMBYTEN2(int8_t,int8_t) (directxpackedvector.h)
description: Initializes a new instance of XMBYTEN2 from two int8_t arguments.
helpviewer_keywords: ["XMBYTEN2","XMBYTEN2 constructor [DirectX Math Support APIs]","XMBYTEN2 constructor [DirectX Math Support APIs]","XMBYTEN2 structure","XMBYTEN2 structure [DirectX Math Support APIs]","XMBYTEN2 constructor","XMBYTEN2.XMBYTEN2","XMBYTEN2.XMBYTEN2(int8_t","int8_t)","XMBYTEN2::XMBYTEN2","XMBYTEN2::XMBYTEN2(int8_t","int8_t)","dxmath.xmbyten2_ctor_3"]
old-location: dxmath\xmbyten2_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMBYTEN2.#ctor(int8_t,int8_t)
ms.date: 12/05/2018
ms.keywords: XMBYTEN2, XMBYTEN2 constructor [DirectX Math Support APIs], XMBYTEN2 constructor [DirectX Math Support APIs],XMBYTEN2 structure, XMBYTEN2 structure [DirectX Math Support APIs],XMBYTEN2 constructor, XMBYTEN2.XMBYTEN2, XMBYTEN2.XMBYTEN2(int8_t,int8_t), XMBYTEN2::XMBYTEN2, XMBYTEN2::XMBYTEN2(int8_t,int8_t), dxmath.xmbyten2_ctor_3
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
 - XMBYTEN2::XMBYTEN2
 - directxpackedvector/XMBYTEN2::XMBYTEN2
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
 - XMBYTEN2.XMBYTEN2
---

# XMBYTEN2::XMBYTEN2(int8_t,int8_t)


## -description

Initializes a new instance of <code>XMBYTEN2</code> from two <code>int8_t</code> arguments.

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyten2">XMBYTEN2 </a> from two <code>int8_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available with C++.</div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new <code>XMBYTEN2</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new <code>XMBYTEN2</code> instance.

## -remarks

Input values are not normalized. The following pseudocode demonstrates the operation of this constructor:


```

	    XMBYTEN2 instance;

	    instance.x = _x; 
	    instance.y = _y; 
	
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyten2">XMBYTEN2</a>



<a href="/windows/desktop/dxmath/xmbyten2-ctor">XMBYTEN2 Constructors</a>