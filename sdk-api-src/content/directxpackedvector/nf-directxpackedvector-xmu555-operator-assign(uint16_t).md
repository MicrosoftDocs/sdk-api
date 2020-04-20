---
UID: NF:directxpackedvector.XMU555.operator-assign(uint16_t)
title: XMU555::operator-assign(uint16_t) (directxpackedvector.h)
description: Assigns the vector component data packed in an instance of uint16_t to the current instance of XMU555.helpviewer_keywords: ["XMU555 structure [DirectX Math Support APIs]","operator = method","XMU555.operator =(const uint16_t)","XMU555.operator-assign(uint16_t)","XMU555.operator=","XMU555::operator-assign(uint16_t)","XMU555::operator=","dxmath.xmu555_operator_eq_2","operator = method [DirectX Math Support APIs]","operator = method [DirectX Math Support APIs]","XMU555 structure","operator="]
old-location: dxmath\xmu555_operator_eq_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMU555.operator = (const uint16_t)
ms.date: 12/05/2018
ms.keywords: XMU555 structure [DirectX Math Support APIs],operator = method, XMU555.operator =(const uint16_t), XMU555.operator-assign(uint16_t), XMU555.operator=, XMU555::operator-assign(uint16_t), XMU555::operator=, dxmath.xmu555_operator_eq_2, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMU555 structure, operator=
f1_keywords:
- directxpackedvector/XMU555.operator =
dev_langs:
- c++
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
- XMU555.operator =
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMU555::operator-assign(uint16_t)


## -description


Assigns the vector component data packed in an instance of <code>uint16_t</code> to the current
	instance of <code>XMU555</code>.
    

Assigns the vector component data packed in an instance of <code>uint16_t</code> to the current
	instance of <a href="https://msdn.microsoft.com/e3cc449d-4db8-402e-9d92-38ae5022deaf">XMU555</a>.
<div class="alert"><b>Note</b>  This operator is only available under C++.
    </div><div> </div>

## -parameters




### -param Packed

The values of four vector components in a packed format.
	    


## -returns



 The current instance of <code>XMU555</code> whose
	    vector component data has been updated to the component values packed in the
	    <code>uint16_t</code> instance specified by the <b>Packed</b> argument.
	    




## -remarks



The format of <b>Packed</b> is:
	

<ul>
<li>
The first 5 bits (bits 0-4) of <b>Packed</b> assigned to the <b>x</b>member of the current instance of <code>XMU555</code>.
		

</li>
<li>
The second 5 bits (bits 5-9) of <b>Packed</b> assigned to the
		    <b>y</b> member of the current instance of <code>XMU555</code>.
		

</li>
<li>
The third 5 bits (bits 10-14) of <b>Packed</b> assigned to the <b>z</b>member of the current instance of <code>XMU555</code>.
		

</li>
<li>
The last 1 bits (bit 15) of <b>Packed</b> assigned to the <b>w</b>member of the current instance of <code>XMU555</code>.
		

</li>
</ul>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/e3cc449d-4db8-402e-9d92-38ae5022deaf">XMU555</a>



<a href="https://msdn.microsoft.com/f2deb13c-c389-461e-aba7-2520b454d46e">operator = </a>
 

 

