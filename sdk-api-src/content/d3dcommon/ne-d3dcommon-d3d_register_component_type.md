---
UID: NE:d3dcommon.D3D_REGISTER_COMPONENT_TYPE
title: D3D_REGISTER_COMPONENT_TYPE
author: windows-sdk-content
description: Values that identify the data types that can be stored in a register.
old-location: direct3d11\d3d_register_component_type.htm
old-project: direct3d11
ms.assetid: 71e3c707-745b-40b4-ba3c-6c501196e3d3
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: D3D10_REGISTER_COMPONENT_FLOAT32, D3D10_REGISTER_COMPONENT_SINT32, D3D10_REGISTER_COMPONENT_UINT32, D3D10_REGISTER_COMPONENT_UNKNOWN, D3D_REGISTER_COMPONENT_FLOAT32, D3D_REGISTER_COMPONENT_SINT32, D3D_REGISTER_COMPONENT_TYPE, D3D_REGISTER_COMPONENT_TYPE enumeration [Direct3D 11], D3D_REGISTER_COMPONENT_UINT32, D3D_REGISTER_COMPONENT_UNKNOWN, d3dcommon/D3D10_REGISTER_COMPONENT_FLOAT32, d3dcommon/D3D10_REGISTER_COMPONENT_SINT32, d3dcommon/D3D10_REGISTER_COMPONENT_UINT32, d3dcommon/D3D10_REGISTER_COMPONENT_UNKNOWN, d3dcommon/D3D_REGISTER_COMPONENT_FLOAT32, d3dcommon/D3D_REGISTER_COMPONENT_SINT32, d3dcommon/D3D_REGISTER_COMPONENT_TYPE, d3dcommon/D3D_REGISTER_COMPONENT_UINT32, d3dcommon/D3D_REGISTER_COMPONENT_UNKNOWN, direct3d11.d3d_register_component_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3dcommon.h
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
req.typenames: D3D_REGISTER_COMPONENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3DCommon.h
api_name:
-	D3D_REGISTER_COMPONENT_TYPE
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# D3D_REGISTER_COMPONENT_TYPE enumeration


## -description


Values that identify the data types that can be stored in a register.


## -enum-fields




### -field D3D_REGISTER_COMPONENT_UNKNOWN

The data type is unknown.


### -field D3D_REGISTER_COMPONENT_UINT32

32-bit unsigned integer.


### -field D3D_REGISTER_COMPONENT_SINT32

32-bit signed integer.


### -field D3D_REGISTER_COMPONENT_FLOAT32

32-bit floating-point number.


### -field D3D10_REGISTER_COMPONENT_UNKNOWN

The data type is unknown.


### -field D3D10_REGISTER_COMPONENT_UINT32

32-bit unsigned integer.


### -field D3D10_REGISTER_COMPONENT_SINT32

32-bit signed integer.


### -field D3D10_REGISTER_COMPONENT_FLOAT32

32-bit floating-point number.


## -remarks



A register component type is specified in the <b>ComponentType</b> member of the <a href="https://msdn.microsoft.com/3aed2f5f-1cfa-4224-bfcc-7d015e6a2cc0">D3D11_SIGNATURE_PARAMETER_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

