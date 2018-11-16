---
UID: NF:d3d11shader.ID3D11ShaderReflectionType.IsOfType
title: ID3D11ShaderReflectionType::IsOfType
author: windows-sdk-content
description: Indicates whether a variable is of the specified type.
old-location: direct3d11\id3d11shaderreflectiontype_isoftype.htm
tech.root: direct3d11
ms.assetid: 8fa1e926-a3d1-4664-b96d-b393ea74b7c5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 46169c40-2e82-364b-2721-507603e99749, ID3D11ShaderReflectionType interface [Direct3D 11],IsOfType method, ID3D11ShaderReflectionType.IsOfType, ID3D11ShaderReflectionType::IsOfType, IsOfType, IsOfType method [Direct3D 11], IsOfType method [Direct3D 11],ID3D11ShaderReflectionType interface, d3d11shader/ID3D11ShaderReflectionType::IsOfType, direct3d11.id3d11shaderreflectiontype_isoftype
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
 - ID3D11ShaderReflectionType.IsOfType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11shader.h
: 
- ID3D11ShaderReflectionType.IsOfType
: 
---

# ID3D11ShaderReflectionType::IsOfType


## -description


Indicates whether a variable is of the specified type.


## -parameters




### -param pType [in]

Type: <b><a href="https://msdn.microsoft.com/04520be2-2491-4f10-988a-e203659efddf">ID3D11ShaderReflectionType</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/04520be2-2491-4f10-988a-e203659efddf">ID3D11ShaderReflectionType Interface</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if object being queried is equal to or inherits from the type in the <i>pType</i> parameter; otherwise returns S_FALSE.




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/04520be2-2491-4f10-988a-e203659efddf">ID3D11ShaderReflectionType Interface</a>
 

 

