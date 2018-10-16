---
UID: NS:dxva2api._DXVA2_Fixed32
title: "_DXVA2_Fixed32"
author: windows-sdk-content
description: Defines a 32-bit fixed-point number.
old-location: mf\dxva2_fixed32.htm
tech.root: medfound
ms.assetid: 5f8f4515-1cf4-4060-813b-c746649c5c40
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: 5f8f4515-1cf4-4060-813b-c746649c5c40, DXVA2_Fixed32, DXVA2_Fixed32 structure [Media Foundation], _DXVA2_Fixed32, dxva2api/DXVA2_Fixed32, mf.dxva2_fixed32
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_Fixed32
product: Windows
targetos: Windows
req.typenames: DXVA2_Fixed32
req.redist: 
---

# _DXVA2_Fixed32 structure


## -description



Defines a 32-bit fixed-point number.




## -struct-fields




### -field Fraction

Fractional part of the number.


### -field Value

Integer part of the number.


### -field ll

Accesses the entire 32 bits of the number. You can use this member to compare <b>DXVA2_Fixed32</b> values.


## -remarks



To convert between floating-point numbers and <b>DXVA2_Fixed32</b> values, use the <a href="https://msdn.microsoft.com/f92c1d78-a2a7-469e-926a-7ba5ad8221e1">DXVA2FixedToFloat</a> and <a href="https://msdn.microsoft.com/2537e691-2137-4e4b-90a0-6749a6ceb144">DXVA2FloatToFixed</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

