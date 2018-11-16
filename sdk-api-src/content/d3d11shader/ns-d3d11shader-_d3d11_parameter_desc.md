---
UID: NS:d3d11shader._D3D11_PARAMETER_DESC
title: "_D3D11_PARAMETER_DESC"
author: windows-sdk-content
description: Describes a function parameter.
old-location: direct3d11\d3d11_parameter_desc.htm
tech.root: direct3d11
ms.assetid: C6F1079C-A686-44EA-933B-9DE2D70CFA33
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D11_PARAMETER_DESC, D3D11_PARAMETER_DESC structure [Direct3D 11], _D3D11_PARAMETER_DESC, d3d11shader/D3D11_PARAMETER_DESC, direct3d11.d3d11_parameter_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11shader.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11Shader.h
api_name:
 - D3D11_PARAMETER_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_PARAMETER_DESC
req.redist: 
---

# _D3D11_PARAMETER_DESC structure


## -description


Describes a function parameter. 


## -struct-fields




### -field Name

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the function parameter.


### -field SemanticName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The HLSL <a href="https://msdn.microsoft.com/6f5c504c-1940-4d1c-b594-a2132599376b">semantic</a> that is associated with this function parameter. This name includes the index, for example, SV_Target[n].


### -field Type

Type: <b><a href="https://msdn.microsoft.com/ef07a68c-d944-4dbb-8cb1-c50403c6c8e8">D3D_SHADER_VARIABLE_TYPE</a></b>

A <a href="https://msdn.microsoft.com/ef07a68c-d944-4dbb-8cb1-c50403c6c8e8">D3D_SHADER_VARIABLE_TYPE</a>-typed value that identifies the variable type for the parameter.


### -field Class

Type: <b><a href="https://msdn.microsoft.com/d367ba01-e357-468d-9417-7d5a282d5565">D3D_SHADER_VARIABLE_CLASS</a></b>

A <a href="https://msdn.microsoft.com/d367ba01-e357-468d-9417-7d5a282d5565">D3D_SHADER_VARIABLE_CLASS</a>-typed value that identifies the variable class for the parameter as one of scalar, vector, matrix, object, and so on.


### -field Rows

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of rows for a matrix parameter.


### -field Columns

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of columns for a matrix parameter.


### -field InterpolationMode

Type: <b><a href="https://msdn.microsoft.com/E4D5F0C3-535F-4CE0-B42F-00D961C83EF1">D3D_INTERPOLATION_MODE</a></b>

A <a href="https://msdn.microsoft.com/E4D5F0C3-535F-4CE0-B42F-00D961C83EF1">D3D_INTERPOLATION_MODE</a>-typed value that identifies the interpolation mode for the parameter.


### -field Flags

Type: <b><a href="https://msdn.microsoft.com/36D757E7-2960-43E3-8C5E-8B11F0109ACD">D3D_PARAMETER_FLAGS</a></b>

A combination of <a href="https://msdn.microsoft.com/36D757E7-2960-43E3-8C5E-8B11F0109ACD">D3D_PARAMETER_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies semantic flags for the parameter.


### -field FirstInRegister

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The first input register for this parameter.


### -field FirstInComponent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The first input register component for this parameter.


### -field FirstOutRegister

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The first output register for this parameter.


### -field FirstOutComponent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The first output register component for this parameter.


## -remarks



Get a function-parameter description by calling <a href="https://msdn.microsoft.com/54755DEE-B865-4C9C-A38F-52749037DBBF">ID3D11FunctionParameterReflection::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/54755DEE-B865-4C9C-A38F-52749037DBBF">ID3D11FunctionParameterReflection::GetDesc</a>



<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

