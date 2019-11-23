---
UID: NF:directxpackedvector.XMUBYTE4.XMUBYTE4(uint32_t)
title: XMUBYTE4::XMUBYTE4(uint32_t) (directxpackedvector.h)

description: Initializes a new instance of XMUBYTE4 from a <Uuint32_t variable containing component data in a packed format.
old-location: 
tech.root: dxmath
ms.assetid: c697b7de-c2b4-4447-9a5a-4813ab37acdc

ms.date: 05/06/2019
ms.keywords: XMUBYTE4, XMUBYTE4 constructor [DirectX Math Support APIs], XMUBYTE4 constructor [DirectX Math Support APIs],XMUBYTE4 structure, XMUBYTE4 structure [DirectX Math Support APIs],XMUBYTE4 constructor, XMUBYTE4.XMUBYTE4, XMUBYTE4.XMUBYTE4(), XMUBYTE4.XMUBYTE4(uint32_t), XMUBYTE4::XMUBYTE4, XMUBYTE4::XMUBYTE4(uint32_t), dxmath.xmubyte4_ctor_1
ms.topic: method
f1_keywords: 
 - "directxpackedvector/XMUBYTE4.XMUBYTE4"
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
 - XMUBYTE4.XMUBYTE4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMUBYTE4::XMUBYTE4(uint32_t)

## -description

Initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte4">XMUBYTE4</a> from a <code>Uuint32_t</code> variable containing component data in a packed format.

This constructor initializes a new instance of **XMUBYTE4** from a <code>Uuint32_t</code> variable containing component data in a packed format.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param Packed

The values of four vector components of the new instance, in a packed format.

## -remarks

The values of the four components of the new instance of **XMUBYTE4* are stored in the argument *Packed* as follows:

* The first 8 bits (bits 0-7) of *Packed* assigned, as an signed integer, to the **x** member of the instance of **XMUBYTE4** constructed.
* The second 8 bits (bits 8-15) of *Packed* assigned, as an signed integer, to the **y** member of the instance of **XMUBYTE4** constructed.
* The third 8 bits (bits 16-23) of *Packed* assigned, as an signed integer, to the **z**  member of the instance of **XMUBYTE4** constructed.
* The last 8 bits (bits 24-31) of *Packed* assigned, as an signed integer, to the **w** member of the instance of **XMUBYTE4** constructed.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte4">XMUBYTE4</a>

<a href="https://docs.microsoft.com/windows/desktop/dxmath/xmubyte4-ctor">XMUBYTE4 Constructors</a>
