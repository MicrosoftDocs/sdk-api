---
UID: NF:d2d1effectauthor_1.ID2D1EffectContext1.CreateLookupTable3D
title: ID2D1EffectContext1::CreateLookupTable3D
author: windows-sdk-content
description: Creates a 3D lookup table for mapping a 3-channel input to a 3-channel output. The table data must be provided in 4-channel format.
old-location: direct2d\id2d1effectcontext1_createlookuptable3d.htm
tech.root: Direct2D
ms.assetid: 410D6785-944D-4A64-887A-0BD4511127DF
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CreateLookupTable3D, CreateLookupTable3D method [Direct2D], CreateLookupTable3D method [Direct2D],ID2D1EffectContext1 interface, ID2D1EffectContext1 interface [Direct2D],CreateLookupTable3D method, ID2D1EffectContext1.CreateLookupTable3D, ID2D1EffectContext1::CreateLookupTable3D, d2d1effectauthor_1/ID2D1EffectContext1::CreateLookupTable3D, direct2d.id2d1effectcontext1_createlookuptable3d
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor_1.h
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
req.lib: D2D1.lib
req.dll: D2D1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.dll
api_name:
 - ID2D1EffectContext1.CreateLookupTable3D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext1::CreateLookupTable3D


## -description


Creates a 3D lookup table for mapping a 3-channel input to a 3-channel output.
        The table data must be provided in 4-channel format.


## -parameters




### -param precision

Type: <b><a href="https://msdn.microsoft.com/a2a4b4fd-685d-4068-b1f5-609e6ab024e2">D2D1_BUFFER_PRECISION</a></b>

Precision of the input lookup table data.


### -param extents [in]

Type: <b>const UINT32*</b>

Number of lookup table elements per dimension (X, Y, Z).


### -param data [in]

Type: <b>const BYTE*</b>

Buffer holding the lookup table data.


### -param dataCount

Type: <b>UINT32</b>

Size of the lookup table data buffer.


### -param strides [in]

Type: <b>const UINT32*</b>

An array containing two values. The first value is the size in bytes from one row (X dimension) of LUT data to the next. 
          The second value is the size in bytes from one LUT data plane (X and Y dimensions) to the next.


### -param lookupTable [out]

Type: <b><a href="https://msdn.microsoft.com/778D2F30-0328-4AA2-8ECA-F443D57809D7">ID2D1LookupTable3D</a>**</b>

Receives the new lookup table instance.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/F6B92F9F-D5F3-4DA9-AEC4-826856E184AF">ID2D1EffectContext1</a>
 

 

