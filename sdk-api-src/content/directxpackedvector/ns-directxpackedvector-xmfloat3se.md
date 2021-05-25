---
UID: NS:directxpackedvector.XMFLOAT3SE
title: XMFLOAT3SE (directxpackedvector.h)
description: Describes a 3D vector of three floating-point components with 9 bit mantissas, each sharing the same 5-bit exponent.
helpviewer_keywords: ["XMFLOAT3SE","XMFLOAT3SE structure [DirectX Math Support APIs]","directxpackedvector/XMFLOAT3SE","dxmath.xmfloat3se"]
old-location: dxmath\xmfloat3se.htm
tech.root: dxmath
ms.assetid: T:Microsoft.directx_sdk.reference.XMFLOAT3SE
ms.date: 12/05/2018
ms.keywords: XMFLOAT3SE, XMFLOAT3SE structure [DirectX Math Support APIs], directxpackedvector/XMFLOAT3SE, dxmath.xmfloat3se
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
 - XMFLOAT3SE
 - directxpackedvector/XMFLOAT3SE
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
 - XMFLOAT3SE
---

## -description

Describes a 3D vector of three floating-point components with 9 bit mantissas, each sharing
	the same 5-bit exponent.

For a list of additional functionality such as constructors and operators that are available
	using <code>XMFLOAT3SE</code> when you are programming in C++, see <a href="/windows/desktop/dxmath/ovw-xmfloat3se-extensions">XMFLOAT3SE Extensions</a>.

## -struct-fields

### -field v

Unsigned 32-bit integer representing the 3D vector.

### -field e : 5

The 5-bit shared exponent.

### -field xm : 9

The 9-bit x component.

### -field ym : 9

The 9-bit y component.

### -field zm : 9

The 9-bit z component.

## -remarks

The values of the three components of an instance of <code>XMFLOAT3SE</code> are stored in
	    the <b>v</b> of the instance in the following format: the <b>e</b> member of the
	    <code>XMFLOAT3SE</code> structure -- the exponent shared by the mantissas of the
	    floating point values of all three components of <code>XMFLOAT3SE</code> -- is
	    stored in the highest order bits of the return value, and the mantissa of the x
	    component stored in the least significant bits.
	


```

   (E5Z9Y9X9): [31] EEEEEzzz zzzzzzyy yyyyyyyx xxxxxxxx [0]

```


Or in detail:
       

<ul>
<li>
Bits 0-8 of <b>Packed</b> are the 9 bit <i>mantissa</i> of the
		   <b>x</b> component's floating point value: the <b>xm</b> member of the current
		   structure.
	       

</li>
<li>
Bits 9-17 of <b>Packed</b> are the 9 bit <i>mantissa</i> of the
		   <b>y</b> component's floating point value: the <b>ym</b> member of the current
		   structure.
	       

</li>
<li>
Bits 18-26 of <b>Packed</b> are the 9 bit <i>mantissa</i> of the
		   <b>z</b> component's floating point value: the <b>zm</b> member of the current
		   structure.
	       

</li>
<li>
Bits 27-31 of <b>Packed</b> are the 5 bit <i>exponent</i> used with
		   the stored mantissas (<b>xm</b>, <b>ym</b>, <b>zm</b>) to represent the size
		   of each component: the <b>e</b> member of the current structure.
	       

</li>
</ul>
As there are no sign bits in the format for storing the components in the <code>XMFLOAT3SE</code> structure, all component values are positive.
       

<code>XMFLOAT3SE</code> can be loaded into instances of <a href="/windows/desktop/dxmath/xmvector-data-type">XMVECTOR</a> by using <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmloadfloat3se">XMLoadFloat3SE</a>.
       

Instances of <code>XMVECTOR</code> can be stored into an instance of <code>XMFLOAT3SE</code> with <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmstorefloat3se">XMStoreFloat3SE</a>.
       

<b>Namespace:</b> Use DirectX::PackedVector

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-structures">DirectXMath Library Structures</a>



<a href="/windows/desktop/dxmath/ovw-xmfloat3se-extensions">XMFLOAT3SE Extensions</a>