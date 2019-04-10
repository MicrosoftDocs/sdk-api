---
UID: NE:d2d1_1.D2D1_BUFFER_PRECISION
title: D2D1_BUFFER_PRECISION (d2d1_1.h)
author: windows-sdk-content
description: Represents the bit depth of the imaging pipeline in Direct2D.
old-location: direct2d\__d2d1_buffer_precision.htm
tech.root: Direct2D
ms.assetid: a2a4b4fd-685d-4068-b1f5-609e6ab024e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D2D1_BUFFER_PRECISION, D2D1_BUFFER_PRECISION enumeration [Direct2D], D2D1_BUFFER_PRECISION_16BPC_FLOAT, D2D1_BUFFER_PRECISION_16BPC_UNORM, D2D1_BUFFER_PRECISION_32BPC_FLOAT, D2D1_BUFFER_PRECISION_8BPC_UNORM, D2D1_BUFFER_PRECISION_8BPC_UNORM_SRGB, D2D1_BUFFER_PRECISION_FORCE_DWORD, D2D1_BUFFER_PRECISION_UNKNOWN, d2d1_1/D2D1_BUFFER_PRECISION, d2d1_1/D2D1_BUFFER_PRECISION_16BPC_FLOAT, d2d1_1/D2D1_BUFFER_PRECISION_16BPC_UNORM, d2d1_1/D2D1_BUFFER_PRECISION_32BPC_FLOAT, d2d1_1/D2D1_BUFFER_PRECISION_8BPC_UNORM, d2d1_1/D2D1_BUFFER_PRECISION_8BPC_UNORM_SRGB, d2d1_1/D2D1_BUFFER_PRECISION_FORCE_DWORD, d2d1_1/D2D1_BUFFER_PRECISION_UNKNOWN, direct2d.__d2d1_buffer_precision
ms.topic: enum
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - D2d1_1.h
api_name:
 - D2D1_BUFFER_PRECISION
product: Windows
targetos: Windows
req.typenames: D2D1_BUFFER_PRECISION
req.redist: 
---

# D2D1_BUFFER_PRECISION enumeration


## -description


Represents the bit depth of the imaging pipeline in Direct2D.


## -enum-fields




### -field D2D1_BUFFER_PRECISION_UNKNOWN

The buffer precision is not specified.


### -field D2D1_BUFFER_PRECISION_8BPC_UNORM

Use 8-bit normalized integer per channel.


### -field D2D1_BUFFER_PRECISION_8BPC_UNORM_SRGB

Use 8-bit normalized integer standard RGB data per channel.


### -field D2D1_BUFFER_PRECISION_16BPC_UNORM

Use 16-bit normalized integer per channel.


### -field D2D1_BUFFER_PRECISION_16BPC_FLOAT

Use 16-bit floats per channel.


### -field D2D1_BUFFER_PRECISION_32BPC_FLOAT

Use 32-bit floats per channel.


### -field D2D1_BUFFER_PRECISION_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.

Do not use this value.


## -remarks



<div class="alert"><b>Note</b>   Feature level 9 may or may not support precision types other than 8BPC.
</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e563cbb0-2ee0-43d8-978c-0bde1950a926">D2D1_RENDERING_CONTROLS</a>



<a href="https://msdn.microsoft.com/b1d15530-a525-42ba-bc58-f8f429cdd2a8">ID2D1DeviceContext::GetRenderingControls</a>



<a href="https://msdn.microsoft.com/6a066126-89d0-4372-bc01-6b6fa1d65440">ID2D1DeviceContext::SetRenderingControls</a>
 

 

