---
UID: NF:directxpackedvector.XMFLOAT3PK.XMFLOAT3PK(XMFLOAT3PK &&)
title: XMFLOAT3PK::XMFLOAT3PK(XMFLOAT3PK &&) (directxpackedvector.h)
description: Assigns the vector component data from one instance of XMFLOAT3SE to the current instance of XMFLOAT3SE.helpviewer_keywords: ["XMFLOAT3PK","XMFLOAT3PK.XMFLOAT3PK","XMFLOAT3PK.XMFLOAT3PK(XMFLOAT3PK &&)","XMFLOAT3PK::XMFLOAT3PK","XMFLOAT3PK::XMFLOAT3PK(XMFLOAT3PK &&)","XMFLOAT3SE structure [DirectX Math Support APIs]","operator = method","XMFLOAT3SE.operator =(const XMFLOAT3SE&)","dxmath.xmfloat3se_operator_eq_1","operator = method [DirectX Math Support APIs]","operator = method [DirectX Math Support APIs]","XMFLOAT3SE structure"]
old-location: dxmath\xmfloat3se_operator_eq_1.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3SE.operator = (const XMFLOAT3SE)
ms.date: 05/06/2019
ms.keywords: XMFLOAT3PK, XMFLOAT3PK.XMFLOAT3PK, XMFLOAT3PK.XMFLOAT3PK(XMFLOAT3PK &&), XMFLOAT3PK::XMFLOAT3PK, XMFLOAT3PK::XMFLOAT3PK(XMFLOAT3PK &&), XMFLOAT3SE structure [DirectX Math Support APIs],operator = method, XMFLOAT3SE.operator =(const XMFLOAT3SE&), dxmath.xmfloat3se_operator_eq_1, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMFLOAT3SE structure
f1_keywords:
- directxpackedvector/XMFLOAT3SE.operator =
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
- XMFLOAT3SE.operator =
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMFLOAT3PK::XMFLOAT3PK(XMFLOAT3PK &&)

## -description

Assigns the vector component data from one instance of <code>XMFLOAT3SE</code> to the current instance of <code>XMFLOAT3SE</code>.

This operator assigns the vector component data from one instance of <a href="https://msdn.microsoft.com/A0FE96C6-42AB-411D-874E-E02E0E81CAF0">XMFLOAT3SE</a> to the current instance of <code>XMFLOAT3SE</code>.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param arg1

Instance of <code>XMFLOAT3SE</code> used to update the current <code>XMFLOAT3SE</code> structure.

## -returns

The current instance of <code>XMFLOAT3SE</code> whose vector component data has been updated to match those of the <code>XMFLOAT3SE</code> instance specified by the <b>float3se</b>argument.

## -see-also

<a href="https://msdn.microsoft.com/A0FE96C6-42AB-411D-874E-E02E0E81CAF0">XMFLOAT3SE</a>

<a href="https://msdn.microsoft.com/e3c74a38-65ab-48ac-931d-1fc66ec04d74">operator = </a>
