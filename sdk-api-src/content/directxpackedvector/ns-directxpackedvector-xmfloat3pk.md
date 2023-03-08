---
UID: NS:directxpackedvector.XMFLOAT3PK
title: XMFLOAT3PK (directxpackedvector.h)
description: Describes a 3D vector with X and Y components stored as 11 bit floating point number, and Z component stored as a 10 bit floating-point value.
helpviewer_keywords: ["XMFLOAT3PK","XMFLOAT3PK structure [DirectX Math Support APIs]","directxpackedvector/XMFLOAT3PK","dxmath.xmfloat3pk"]
old-location: dxmath\xmfloat3pk.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMFLOAT3PK
ms.date: 12/05/2018
ms.keywords: XMFLOAT3PK, XMFLOAT3PK structure [DirectX Math Support APIs], directxpackedvector/XMFLOAT3PK, dxmath.xmfloat3pk
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
req.namespace: 
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
 - XMFLOAT3PK
 - directxpackedvector/XMFLOAT3PK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectXPackedVector.h
api_name:
 - XMFLOAT3PK
---

## -description

Describes a 3D vector with X and Y components stored as 11 bit floating point number, and Z
	component stored as a 10 bit floating-point value.

For a list of additional functionality, such as constructors and operators, available using
	<code>XMFLOAT3PK</code> when programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmfloat3pk-extensions">XMFLOAT3PK Extensions</a>.

## -struct-fields

### -field v

Unsigned 32-bit integer representing the 3D vector.

### -field xe : 5

The 5-bit biased exponent for the x component.

### -field xm : 6

The 6-bit mantissa for the x component.

### -field ye : 5

The 5-bit biased exponent for the y component.

### -field ym : 6

The 6-bit mantissa for the y component.

### -field ze : 5

The 5-bit biased exponent for the z component.

### -field zm : 5

The 5-bit mantissa for the z component.

## -remarks

There are no sign bits. This means all partial-precision numbers are positive. The z
	    component is stored in the most significant bits, and the x component is stored in the
	    least significant bits like this:

```
(Z10Y11X11): [31] ZZZZZzzz zzYYYYYy yyyyyXXX XXxxxxxx [0]
```

Or in detail:
     

<ul>
<li>
Bits 0-5 of <b>v</b> are the 6 bit <i>mantissa</i> of the <b>x</b> component's floating point value: the <b>xm</b> member of the structure.
	     

</li>
<li>
Bits 6-10 of <b>v</b> are the 5 bit <i>exponent</i> of the
		 <b>x</b> component's floating point value the <b>xe</b> member of the structure.
	     

</li>
<li>
Bits 11-16 of <b>v</b> are the 6-bit <i>mantissa</i> of the
		 <b>y</b> component's floating point value: the <b>ym</b> member of the
		 structure.
	     

</li>
<li>
Bits 17-21 of <b>v</b> are the 5 bit <i>exponent</i> of the
		 <b>y</b> component's floating point value: the <b>ye</b> member of the
		 structure.
	     

</li>
<li>
Bits 22-26 of <b>v</b> are the 5 bit <i>mantissa</i> of the
		 <b>z</b> component's floating point value: the <b>zm</b> member of the
		 structure.
	     

</li>
<li>
Bits 27-31 of <b>v</b> are the 5 bit <i>exponent</i> of the
		 <b>z</b> component's floating point value: the <b>ze</b> member of the
		 structure.
	     

</li>
</ul>
<code>XMFLOAT3PK</code> can be loaded into instances of <a href="/windows/desktop/dxmath/xmvector-data-type"> XMVECTOR</a> by using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadfloat3pk">XMLoadFloat3PK</a>.


Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMFLOAT3PK</code> with <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstorefloat3pk">XMStoreFloat3PK</a>.


MIN_F10 / MIN_F11 = 6.10352e-5

MAX_F10 = 64512

MAX_F11 = 65024

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmfloat3pk-extensions">XMFLOAT3PK Extensions</a>