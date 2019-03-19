---
UID: NE:d3dcommon.D3D_MIN_PRECISION
title: D3D_MIN_PRECISION (d3dcommon.h)
author: windows-sdk-content
description: Values that indicate the minimum desired interpolation precision.
old-location: direct3d11\d3d_min_precision.htm
tech.root: direct3d11
ms.assetid: C97D04D7-EAE4-4E5B-80A2-EDB1CE68C2BC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D_MIN_PRECISION, D3D_MIN_PRECISION enumeration [Direct3D 11], D3D_MIN_PRECISION_ANY_10, D3D_MIN_PRECISION_ANY_16, D3D_MIN_PRECISION_DEFAULT, D3D_MIN_PRECISION_FLOAT_16, D3D_MIN_PRECISION_FLOAT_2_8, D3D_MIN_PRECISION_RESERVED, D3D_MIN_PRECISION_SINT_16, D3D_MIN_PRECISION_UINT_16, d3dcommon/D3D_MIN_PRECISION, d3dcommon/D3D_MIN_PRECISION_ANY_10, d3dcommon/D3D_MIN_PRECISION_ANY_16, d3dcommon/D3D_MIN_PRECISION_DEFAULT, d3dcommon/D3D_MIN_PRECISION_FLOAT_16, d3dcommon/D3D_MIN_PRECISION_FLOAT_2_8, d3dcommon/D3D_MIN_PRECISION_RESERVED, d3dcommon/D3D_MIN_PRECISION_SINT_16, d3dcommon/D3D_MIN_PRECISION_UINT_16, direct3d11.d3d_min_precision
ms.topic: enum
req.header: d3dcommon.h
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
 - D3DCommon.h
api_name:
 - D3D_MIN_PRECISION
product: Windows
targetos: Windows
req.typenames: D3D_MIN_PRECISION
req.redist: 
---

# D3D_MIN_PRECISION enumeration


## -description


Values that indicate the minimum desired interpolation precision.


## -enum-fields




### -field D3D_MIN_PRECISION_DEFAULT

Default minimum precision, which is 32-bit precision.


### -field D3D_MIN_PRECISION_FLOAT_16

Minimum precision is min16float, which is 16-bit floating point. 


### -field D3D_MIN_PRECISION_FLOAT_2_8

Minimum precision is min10float, which is 10-bit floating point. 


### -field D3D_MIN_PRECISION_RESERVED

Reserved


### -field D3D_MIN_PRECISION_SINT_16

Minimum precision is min16int, which is 16-bit signed integer. 


### -field D3D_MIN_PRECISION_UINT_16

Minimum precision is min16uint, which is 16-bit unsigned integer. 


### -field D3D_MIN_PRECISION_ANY_16

Minimum precision is any 16-bit value. 


### -field D3D_MIN_PRECISION_ANY_10

Minimum precision is any 10-bit value. 


## -remarks



For more info, see <a href="https://msdn.microsoft.com/en-us/library/Bb509646(v=VS.85).aspx">Scalar Types</a> and <a href="https://msdn.microsoft.com/422B0C45-5CEB-4235-AD05-62D36C36CFC6">Using HLSL minimum precision</a>.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

