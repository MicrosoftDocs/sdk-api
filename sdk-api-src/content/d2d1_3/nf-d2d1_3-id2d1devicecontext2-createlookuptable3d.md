---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateLookupTable3D
title: ID2D1DeviceContext2::CreateLookupTable3D
author: windows-sdk-content
description: Creates a 3D lookup table for mapping a 3-channel input to a 3-channel output. The table data must be provided in 4-channel format.
old-location: direct2d\id2d1devicecontext2_createlookuptable3d.htm
tech.root: direct2d
ms.assetid: 1c48804b-9876-9dbd-3d20-8a7b575fd3d8
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: CreateLookupTable3D, CreateLookupTable3D method [Direct2D], CreateLookupTable3D method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateLookupTable3D method, ID2D1DeviceContext2.CreateLookupTable3D, ID2D1DeviceContext2::CreateLookupTable3D, d2d1_3/ID2D1DeviceContext2::CreateLookupTable3D, direct2d.id2d1devicecontext2_createlookuptable3d
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext2.CreateLookupTable3D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext2::CreateLookupTable3D


## -description


Creates a 3D lookup table for mapping a 3-channel input to a 3-channel output. The table data must be provided in 4-channel format.


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

An array containing two values.  The first value is the size in bytes from one row (X dimension) of LUT data to the next.  
          The second value is the size in bytes from one LUT data plane (X and Y dimensions) to the next.


### -param lookupTable [out]

Type: <b><a href="https://msdn.microsoft.com/778D2F30-0328-4AA2-8ECA-F443D57809D7">ID2D1LookupTable3D</a>**</b>

Receives the new lookup table instance.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.




## -see-also




<a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a>
 

 

