---
UID: NE:d3dcommon.D3D_RESOURCE_RETURN_TYPE
title: D3D_RESOURCE_RETURN_TYPE
author: windows-sdk-content
description: Values that identify the return type of a resource.
old-location: direct3d11\d3d_resource_return_type.htm
old-project: direct3d11
ms.assetid: 3da3f315-9f92-4557-93b8-94aff42a91fe
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: D3D10_RETURN_TYPE_FLOAT, D3D10_RETURN_TYPE_MIXED, D3D10_RETURN_TYPE_SINT, D3D10_RETURN_TYPE_SNORM, D3D10_RETURN_TYPE_UINT, D3D10_RETURN_TYPE_UNORM, D3D11_RETURN_TYPE_CONTINUED, D3D11_RETURN_TYPE_DOUBLE, D3D11_RETURN_TYPE_FLOAT, D3D11_RETURN_TYPE_MIXED, D3D11_RETURN_TYPE_SINT, D3D11_RETURN_TYPE_SNORM, D3D11_RETURN_TYPE_UINT, D3D11_RETURN_TYPE_UNORM, D3D_RESOURCE_RETURN_TYPE, D3D_RESOURCE_RETURN_TYPE enumeration [Direct3D 11], D3D_RETURN_TYPE_CONTINUED, D3D_RETURN_TYPE_DOUBLE, D3D_RETURN_TYPE_FLOAT, D3D_RETURN_TYPE_MIXED, D3D_RETURN_TYPE_SINT, D3D_RETURN_TYPE_SNORM, D3D_RETURN_TYPE_UINT, D3D_RETURN_TYPE_UNORM, d3dcommon/D3D10_RETURN_TYPE_FLOAT, d3dcommon/D3D10_RETURN_TYPE_MIXED, d3dcommon/D3D10_RETURN_TYPE_SINT, d3dcommon/D3D10_RETURN_TYPE_SNORM, d3dcommon/D3D10_RETURN_TYPE_UINT, d3dcommon/D3D10_RETURN_TYPE_UNORM, d3dcommon/D3D11_RETURN_TYPE_CONTINUED, d3dcommon/D3D11_RETURN_TYPE_DOUBLE, d3dcommon/D3D11_RETURN_TYPE_FLOAT, d3dcommon/D3D11_RETURN_TYPE_MIXED, d3dcommon/D3D11_RETURN_TYPE_SINT, d3dcommon/D3D11_RETURN_TYPE_SNORM, d3dcommon/D3D11_RETURN_TYPE_UINT, d3dcommon/D3D11_RETURN_TYPE_UNORM, d3dcommon/D3D_RESOURCE_RETURN_TYPE, d3dcommon/D3D_RETURN_TYPE_CONTINUED, d3dcommon/D3D_RETURN_TYPE_DOUBLE, d3dcommon/D3D_RETURN_TYPE_FLOAT, d3dcommon/D3D_RETURN_TYPE_MIXED, d3dcommon/D3D_RETURN_TYPE_SINT, d3dcommon/D3D_RETURN_TYPE_SNORM, d3dcommon/D3D_RETURN_TYPE_UINT, d3dcommon/D3D_RETURN_TYPE_UNORM, direct3d11.d3d_resource_return_type
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
tech.root: 
req.typenames: D3D_RESOURCE_RETURN_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3DCommon.h
api_name:
 - D3D_RESOURCE_RETURN_TYPE
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# D3D_RESOURCE_RETURN_TYPE enumeration


## -description


Values that identify the return type of a resource.


## -enum-fields




### -field D3D_RETURN_TYPE_UNORM

Return type is an unsigned integer value normalized to a value between 0 and 1.


### -field D3D_RETURN_TYPE_SNORM

Return type is a signed integer value normalized to a value between -1 and 1.


### -field D3D_RETURN_TYPE_SINT

Return type is a signed integer.


### -field D3D_RETURN_TYPE_UINT

Return type is an unsigned integer.


### -field D3D_RETURN_TYPE_FLOAT

Return type is a floating-point number.


### -field D3D_RETURN_TYPE_MIXED

Return type is unknown.


### -field D3D_RETURN_TYPE_DOUBLE

Return type is a double-precision value.


### -field D3D_RETURN_TYPE_CONTINUED

Return type is a multiple-dword type, such as a double or uint64, and the component is continued from the previous component that was declared.  The first component represents the lower bits.


### -field D3D10_RETURN_TYPE_UNORM

Unsigned integer value normalized to a value between 0 and 1.


### -field D3D10_RETURN_TYPE_SNORM

Signed integer value normalized to a value between -1 and 1.


### -field D3D10_RETURN_TYPE_SINT

Signed integer.


### -field D3D10_RETURN_TYPE_UINT

Unsigned integer.


### -field D3D10_RETURN_TYPE_FLOAT

Floating-point number.


### -field D3D10_RETURN_TYPE_MIXED

Return type is unknown.


### -field D3D11_RETURN_TYPE_UNORM

Return type is an unsigned integer value normalized to a value between 0 and 1.


### -field D3D11_RETURN_TYPE_SNORM

Return type is a signed integer value normalized to a value between -1 and 1.


### -field D3D11_RETURN_TYPE_SINT

Return type is a signed integer.


### -field D3D11_RETURN_TYPE_UINT

Return type is an unsigned integer.


### -field D3D11_RETURN_TYPE_FLOAT

Return type is a floating-point number.


### -field D3D11_RETURN_TYPE_MIXED

Return type is unknown.


### -field D3D11_RETURN_TYPE_DOUBLE

Return type is a double-precision value.


### -field D3D11_RETURN_TYPE_CONTINUED

Return type is a multiple-dword type, such as a double or uint64, and the component is continued from the previous component that was declared.  The first component represents the lower bits.


## -remarks



A resource return type is specified in the <b>ReturnType</b> member of the <a href="https://msdn.microsoft.com/384ad8f8-0991-4cd2-bb3d-76b8338686da">D3D11_SHADER_INPUT_BIND_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

