---
UID: NF:directxpackedvector.XMFLOAT3PK.operator-assign(XMFLOAT3PK &&)
title: XMFLOAT3PK::operator-assign(XMFLOAT3PK &&) (directxpackedvector.h)
description: Assigns the vector component data from one instance of XMFLOAT3PK to the current instance of XMFLOAT3PK.
old-location: dxmath\xmfloat3pk_operator_eq_1.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3PK.operator = (const XMFLOAT3PK)
ms.date: 05/06/2019
ms.keywords: XMFLOAT3PK structure [DirectX Math Support APIs],operator = method, XMFLOAT3PK.operator =(const XMFLOAT3PK&), XMFLOAT3PK.operator-assign(XMFLOAT3PK &&), XMFLOAT3PK.operator=, XMFLOAT3PK::operator-assign(XMFLOAT3PK &&), XMFLOAT3PK::operator=, dxmath.xmfloat3pk_operator_eq_1, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMFLOAT3PK structure, operator=
f1_keywords:
- directxpackedvector/XMFLOAT3PK.operator =
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
- XMFLOAT3PK.operator =
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMFLOAT3PK::operator-assign(XMFLOAT3PK &&)

## -description

Assigns the vector component data from one instance of <code>XMFLOAT3PK</code> to the current instance of <code>XMFLOAT3PK</code>.

This operator assigns the vector component data from one instance of <a href="https://msdn.microsoft.com/40b3df37-d1c1-43fe-afcb-cbac4d9b6564">XMFLOAT3PK</a> to the current instance of <code>XMFLOAT3PK</code>.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param arg1

Instance of <code>XMFLOAT3PK</code> used to update the current <code>XMFLOAT3PK</code> structure.

## -returns

The current instance of <code>XMFLOAT3PK</code> whose vector component data has been updated to match those of the <code>XMFLOAT3PK</code> instance specified by the <b>float3pk</b>argument.

## -see-also

<a href="https://msdn.microsoft.com/40b3df37-d1c1-43fe-afcb-cbac4d9b6564">XMFLOAT3PK</a>

<a href="https://msdn.microsoft.com/82c6ee72-0706-49f9-bc19-9725496440d0">operator = </a>
