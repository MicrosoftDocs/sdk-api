---
UID: NF:directxpackedvector.XMUDEC4.operator-assign(uint32_t)
title: XMUDEC4::operator=
description: Assigns the vector component data packed in an instance of uint32_t to the current instance of XMUDEC4.
tech.root: dxmath
helpviewer_keywords: ["XMUDEC4::operator="]
ms.assetid: fa7526a5-4fff-46f9-a79a-af2a6c5caacb
ms.date: 05/20/2019
ms.keywords: XMUDEC4::operator=
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: directxpackedvector.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - XMUDEC4::operator=
 - directxpackedvector/XMUDEC4::operator=
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - directxpackedvector.h
api_name:
 - XMUDEC4::operator=
---

# XMUDEC4::operator =  (const uint32_t)


## -description

Assigns the vector component data packed in an instance of **uint32_t** to the current instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudec4">XMUDEC4</a>.

This operator assigns the vector component data packed in an instance of **uint32_t** to the current instance of **XMUDEC4**.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div>

## -parameters

### -param Packed

The values of four vector components in a packed format.

## -returns

The current instance of **XMUDEC4** whose vector component data has been updated to the component values packed in the **uint32_t** instance specified by the *Packed* argument.

## -remarks

The format of Packed is:

* The first 10 bits (bits 0-09) of *Packed* assigned to the **x** member of the current instance of **XMUDEC4**.
* The second 10 bits (bits 10-19) of *Packed* assigned to the **y** member of the current instance of **XMUDEC4**.
* The third 10 bits (bits 10-29) of *Packed* assigned to the **z** member of the current instance of **XMUDEC4**.
* The last 2 bits (bits 30-31) of *Packed* assigned to the **w** member of the current instance of **XMUDEC4**.

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudec4">XMUDEC4</a>