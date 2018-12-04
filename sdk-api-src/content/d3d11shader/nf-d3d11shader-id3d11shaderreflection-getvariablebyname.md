---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetVariableByName
title: ID3D11ShaderReflection::GetVariableByName
author: windows-sdk-content
description: Gets a variable by name.
old-location: direct3d11\id3d11shaderreflection_getvariablebyname.htm
tech.root: direct3d11
ms.assetid: 8c21756f-40f0-4459-852b-445053aa03e8
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 714dbbf5-52e2-8540-c5c1-aa03dcf32bf2, GetVariableByName, GetVariableByName method [Direct3D 11], GetVariableByName method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetVariableByName method, ID3D11ShaderReflection.GetVariableByName, ID3D11ShaderReflection::GetVariableByName, d3d11shader/ID3D11ShaderReflection::GetVariableByName, direct3d11.id3d11shaderreflection_getvariablebyname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ShaderReflection.GetVariableByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ShaderReflection::GetVariableByName


## -description


Gets a variable by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

A pointer to a string containing the variable name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4422a51f-b190-4df0-a1bb-a8ee2cc66da2">ID3D11ShaderReflectionVariable</a>*</b>

Returns a <a href="https://msdn.microsoft.com/4422a51f-b190-4df0-a1bb-a8ee2cc66da2">ID3D11ShaderReflectionVariable Interface</a> interface.
          




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/a28cca72-7f2d-416a-bfa9-4d1f71fc98d5">ID3D11ShaderReflection Interface</a>
 

 

