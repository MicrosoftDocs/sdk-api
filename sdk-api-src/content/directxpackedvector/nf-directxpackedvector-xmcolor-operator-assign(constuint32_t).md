---
UID: NF:directxpackedvector.XMCOLOR.operator-assign(constuint32_t)
title: XMCOLOR::operator-assign(const uint32_t) (directxpackedvector.h)
description: Assigns the vector component data packed in an instance of uint32_t to the current instance of XMCOLOR.
helpviewer_keywords: ["XMCOLOR structure [DirectX Math Support APIs]","operator = method","XMCOLOR.operator =(const uint32_t)","XMCOLOR.operator-assign(const uint32_t)","XMCOLOR.operator=","XMCOLOR::operator-assign(const uint32_t)","XMCOLOR::operator=","dxmath.xmcolor_operator_eq_2","operator = method [DirectX Math Support APIs]","operator = method [DirectX Math Support APIs]","XMCOLOR structure","operator="]
old-location: dxmath\xmcolor_operator_eq_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMCOLOR.operator = (const uint32_t)
ms.date: 12/05/2018
ms.keywords: XMCOLOR structure [DirectX Math Support APIs],operator = method, XMCOLOR.operator =(const uint32_t), XMCOLOR.operator-assign(const uint32_t), XMCOLOR.operator=, XMCOLOR::operator-assign(const uint32_t), XMCOLOR::operator=, dxmath.xmcolor_operator_eq_2, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMCOLOR structure, operator=
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
 - XMCOLOR::operator=
 - directxpackedvector/XMCOLOR::operator=
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
 - XMCOLOR.operator =
---

# XMCOLOR::operator-assign(const uint32_t)


## -description

Assigns the vector component data packed in an instance of <code>uint32_t</code> to the current instance of
  <code>XMCOLOR</code>.

This operator assigns the vector component data packed in an instance of <code>uint32_t</code> to the current instance of
  <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a>.
<div class="alert"><b>Note</b>  This operator is only available under C++.</div><div> </div>

## -parameters

### -param Color

The values of four vector components in a packed format.

## -returns

The current instance of <code>XMCOLOR</code> whose vector component data has been
		updated to the component values packed in the <code>uint32_t</code> instance specified by
		the <b>Color</b> argument.

## -remarks

The format of <b>Color</b> is:

<ul>
<li>
The first 8 bits (bits 0-7) of <b>Color</b> assigned, as an unsigned integer, to the <b>a</b> member (alpha
       channel) of the current instance of <code>XMCOLOR</code>.

</li>
<li>
The second 8 bits (bits 8-15) of <b>Color</b> assigned, as an unsigned integer, to the <b>r</b> member (red
       color channel) of the current instance of <code>XMCOLOR</code>.

</li>
<li>
The third 8 bits (bits 16-23) of <b>Color</b> assigned, as an unsigned integer, to the <b>g</b> member (green
       color channel) of the current instance of <code>XMCOLOR</code>.

</li>
<li>
The fourth 8 bits (bits 24-31) of <b>Color</b> assigned, as an unsigned integer, to the <b>b</b> member (blue
       color channel) of the current instance of <code>XMCOLOR</code>.

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a>



<a href="https://msdn.microsoft.com/7dbba878-2f03-451f-b02b-75e531b6315b">operator = </a>