---
UID: NF:directxpackedvector.XMU565.operator-assign(uint16_t)
title: XMU565::operator-assign(uint16_t) (directxpackedvector.h)
description: Assigns the vector component data packed in an instance of uint16_t to the current instance of XMU565.
helpviewer_keywords: ["XMU565 structure [DirectX Math Support APIs]","operator = method","XMU565.operator =(const uint16_t)","XMU565.operator-assign(uint16_t)","XMU565.operator=","XMU565::operator-assign(uint16_t)","XMU565::operator=","dxmath.xmu565_operator_eq_2","operator = method [DirectX Math Support APIs]","operator = method [DirectX Math Support APIs]","XMU565 structure","operator="]
old-location: dxmath\xmu565_operator_eq_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMU565.operator = (const uint16_t)
ms.date: 12/05/2018
ms.keywords: XMU565 structure [DirectX Math Support APIs],operator = method, XMU565.operator =(const uint16_t), XMU565.operator-assign(uint16_t), XMU565.operator=, XMU565::operator-assign(uint16_t), XMU565::operator=, dxmath.xmu565_operator_eq_2, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMU565 structure, operator=
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
 - XMU565::operator=
 - directxpackedvector/XMU565::operator=
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
 - XMU565.operator =
---

# XMU565::operator-assign(uint16_t)


## -description

Assigns the vector component data packed in an instance of <code>uint16_t</code> to the current
	instance of <code>XMU565</code>.
    

Assigns the vector component data packed in an instance of <code>uint16_t</code> to the current
	instance of <a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565">XMU565</a>.
<div class="alert"><b>Note</b>  This operator is only available under C++.
    </div><div> </div>

## -parameters

### -param Packed

The values of three vector components in a packed format.

## -returns

The current instance of <code>XMU565</code> whose vector component data has been
		updated to the component values packed in the <code>uint16_t</code> instance specified
		by the <b>Packed</b> argument.

## -remarks

The format of <b>Packed</b> is:
	

<ul>
<li>
The first 5 bits (bits 0-4) of <b>Packed</b> assigned to the <b>x</b> member of the current instance of <code>XMU565</code>.
		

</li>
<li>
The second 6 bits (bits 5-10) of <b>Packed</b> assigned to the <b>y</b> member of the current instance of <code>XMU565</code>.
		

</li>
<li>
The third 5 bits (bits 11-15) of <b>Packed</b> assigned to the <b>z</b> member of the current instance of <code>XMU565</code>.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565">XMU565</a>



<a href="https://msdn.microsoft.com/05e80a7b-107a-4355-a057-3315cdf46844">operator = </a>

