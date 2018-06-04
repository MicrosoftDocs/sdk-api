---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

