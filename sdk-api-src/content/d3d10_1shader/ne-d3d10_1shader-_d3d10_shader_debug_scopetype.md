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

# _D3D10_SHADER_DEBUG_SCOPETYPE enumeration


## -description


Scope types.


## -enum-fields




### -field D3D10_SHADER_DEBUG_SCOPE_GLOBAL

Global scope.


### -field D3D10_SHADER_DEBUG_SCOPE_BLOCK

Block scope.


### -field D3D10_SHADER_DEBUG_SCOPE_FORLOOP

For loop scope.


### -field D3D10_SHADER_DEBUG_SCOPE_STRUCT

Structure scope.


### -field D3D10_SHADER_DEBUG_SCOPE_FUNC_PARAMS

Function parameter scope.


### -field D3D10_SHADER_DEBUG_SCOPE_STATEBLOCK

State block scope.


### -field D3D10_SHADER_DEBUG_SCOPE_NAMESPACE

Name space scope.


### -field D3D10_SHADER_DEBUG_SCOPE_ANNOTATION

Annotation scope.


### -field D3D10_SHADER_DEBUG_SCOPE_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.


## -remarks



The <b>D3D10_SHADER_DEBUG_SCOPETYPE</b> enumeration is used to specify scope type in the <a href="https://msdn.microsoft.com/ccee4d4b-86e2-441c-abc1-2aba1163f149">D3D10_SHADER_DEBUG_SCOPE_INFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/8d2b758b-cc2a-43ad-bf26-51674d4b5129">Shader Enumerations</a>
 

 

