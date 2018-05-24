---
UID: NF:d3d10shader.D3D10ReflectShader
title: D3D10ReflectShader function
author: windows-driver-content
description: This function -- which creates a shader-reflection object for retrieving information about a compiled shader -- has been deprecated. Instead, use D3DReflect.
old-location: direct3d10\d3d10reflectshader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10reflectshader.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: D3D10ReflectShader, D3D10ReflectShader function [Direct3D 10], abc201df-57cf-fbbd-708b-94ffa50ba7d4, d3d10shader/D3D10ReflectShader, direct3d10.d3d10reflectshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d3d10shader.h
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
req.typenames: D3D10_MESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	D3D10.dll
api_name:
-	D3D10ReflectShader
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10ReflectShader function


## -description


This function -- which creates a shader-reflection object for retrieving information about a compiled shader -- has been deprecated. Instead, use <a href="https://msdn.microsoft.com/601cc907-2878-4c9b-bc48-0575fd4479e8">D3DReflect</a>.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader.


### -param BytecodeLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of pShaderBytecode.


### -param ppReflector [out]

Type: <b><a href="https://msdn.microsoft.com/097ed643-4e7a-4214-80a1-9a56d1157044">ID3D10ShaderReflection</a>**</b>

Address of a reflection interface.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Return value.




## -see-also




<a href="https://msdn.microsoft.com/c8b33c08-7b3f-4b33-9b3c-4aa2b45b8f32">Shader Functions</a>
 

 

