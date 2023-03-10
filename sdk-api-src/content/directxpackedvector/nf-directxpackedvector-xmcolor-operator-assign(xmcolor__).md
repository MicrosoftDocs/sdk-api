---
UID: NF:directxpackedvector.XMCOLOR.operator-assign(XMCOLOR&&)
title: XMCOLOR::operator-assign(XMCOLOR &&) (directxpackedvector.h)
description: This operator assigns the vector component data from one instance of XMCOLOR to the current instance of XMCOLOR.
helpviewer_keywords: ["XMCOLOR structure [DirectX Math Support APIs]","operator = method","XMCOLOR.operator =(const XMCOLOR&)","XMCOLOR.operator-assign(XMCOLOR &&)","XMCOLOR.operator=","XMCOLOR::operator-assign(XMCOLOR &&)","XMCOLOR::operator=","dxmath.xmcolor_operator_eq_1","operator = method [DirectX Math Support APIs]","operator = method [DirectX Math Support APIs]","XMCOLOR structure","operator="]
old-location: dxmath\xmcolor_operator_eq_1.htm
tech.root: dxmath
ms.assetid: 3ad704a1-8244-4c35-9dc6-0b4058c71caa
ms.date: 05/06/2019
ms.keywords: XMCOLOR structure [DirectX Math Support APIs],operator = method, XMCOLOR.operator =(const XMCOLOR&), XMCOLOR.operator-assign(XMCOLOR &&), XMCOLOR.operator=, XMCOLOR::operator-assign(XMCOLOR &&), XMCOLOR::operator=, dxmath.xmcolor_operator_eq_1, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMCOLOR structure, operator=
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

# XMCOLOR::operator-assign(XMCOLOR &&)


## -description

This operator assigns the vector component data from one instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a> to the current instance of <b>XMCOLOR</b>.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param unnamedParam1

Instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a> used to update the current <b>XMCOLOR</b> structure.

## -returns

 The current instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a> whose vector component data has been updated to match those of the <b>XMCOLOR</b> instance specified by the <i>Color</i> argument.

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a>

<a href="https://msdn.microsoft.com/7dbba878-2f03-451f-b02b-75e531b6315b">operator = </a>