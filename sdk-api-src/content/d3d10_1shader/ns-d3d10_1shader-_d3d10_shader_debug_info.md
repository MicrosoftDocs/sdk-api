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

# _D3D10_SHADER_DEBUG_INFO structure


## -description


Describes the format of the <a href="https://msdn.microsoft.com/d180fee0-1a69-4250-a0c4-d6e3754f063a">ID3D10Blob Interface</a> returned by <a href="https://msdn.microsoft.com/f42def2b-5011-471c-9667-d62a155cc759">D3D10GetShaderDebugInfo</a>.


## -struct-fields




### -field Size

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of this structure.


### -field Creator

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to LPCSTR for compiler version.


### -field EntrypointName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to LPCSTR for Entry point name.


### -field ShaderTarget

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to LPCSTR for shader target.


### -field CompileFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags used to compile.


### -field Files

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of included files.


### -field FileInfo

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to array of <a href="https://msdn.microsoft.com/17927edc-fe1b-4e9b-8963-f310d65ac2d8">D3D10_SHADER_DEBUG_FILE_INFO</a> structures that has <b>Files</b> elements.


### -field Instructions

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of instructions.


### -field InstructionInfo

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to array of <a href="https://msdn.microsoft.com/6bf3ffa3-fdba-428f-87e6-9156cb1604c8">D3D10_SHADER_DEBUG_INST_INFO</a> structures that has <b>Instructions</b> elements.


### -field Variables

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of variables.


### -field VariableInfo

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to array of <a href="https://msdn.microsoft.com/126c1efd-8f41-4b03-8587-21e7d607362b">D3D10_SHADER_DEBUG_VAR_INFO</a> structures that has <b>Variables</b> elements.


### -field InputVariables

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of variables to initialize before running.


### -field InputVariableInfo

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to array of <a href="https://msdn.microsoft.com/143b770a-9ae0-4e2e-9d71-e0d4838070cb">D3D10_SHADER_DEBUG_INPUT_INFO</a> structures that has <b>InputVariables</b> elements.


### -field Tokens

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of tokens to initialize.


### -field TokenInfo

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to array of <a href="https://msdn.microsoft.com/caf2f905-e183-48d6-af3c-2dbb0079fee5">D3D10_SHADER_DEBUG_TOKEN_INFO</a> structures that has <b>Tokens</b> elements.


### -field Scopes

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of scopes.


### -field ScopeInfo

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to array of <a href="https://msdn.microsoft.com/ccee4d4b-86e2-441c-abc1-2aba1163f149">D3D10_SHADER_DEBUG_SCOPE_INFO</a> structures that has <b>Scopes</b> elements.


### -field ScopeVariables

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of variables declared.


### -field ScopeVariableInfo

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to array of <a href="https://msdn.microsoft.com/4ea300b1-fbd6-4cb0-8485-42f55806e19d">D3D10_SHADER_DEBUG_SCOPEVAR_INFO</a> structures that has <b>Scopes</b> elements.


### -field UintOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to the UINT datastore, all UINT offsets are from this offset.


### -field StringOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset to the string datastore, all string offsets are from this offset.


## -see-also




<a href="https://msdn.microsoft.com/b36309e0-1c44-42d9-adcf-33acd753438c">Shader Structures</a>
 

 

