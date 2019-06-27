---
UID: NS:dxva2api._DXVA2_Fixed32
title: DXVA2_Fixed32 (dxva2api.h)
author: windows-sdk-content
description: Defines a 32-bit fixed-point number.
old-location: mf\dxva2_fixed32.htm
tech.root: medfound
ms.assetid: 5f8f4515-1cf4-4060-813b-c746649c5c40
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 5f8f4515-1cf4-4060-813b-c746649c5c40, DXVA2_Fixed32, DXVA2_Fixed32 structure [Media Foundation], dxva2api/DXVA2_Fixed32, mf.dxva2_fixed32
ms.topic: struct
f1_keywords: 
 - "dxva2api/DXVA2_Fixed32"
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
ms.custom: 19H1
---

# DXVA2_Fixed32 structure


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



To convert between floating-point numbers and <b>DXVA2_Fixed32</b> values, use the <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-dxva2fixedtofloat">DXVA2FixedToFloat</a> and <a href="https://docs.microsoft.com/windows/desktop/api/dxva2api/nf-dxva2api-dxva2floattofixed">DXVA2FloatToFixed</a> functions.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
 

 

