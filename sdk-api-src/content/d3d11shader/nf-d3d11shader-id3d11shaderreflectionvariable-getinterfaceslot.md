---
UID: NF:d3d11shader.ID3D11ShaderReflectionVariable.GetInterfaceSlot
title: ID3D11ShaderReflectionVariable::GetInterfaceSlot (d3d11shader.h)
description: Gets the corresponding interface slot for a variable that represents an interface pointer. (ID3D11ShaderReflectionVariable.GetInterfaceSlot)
helpviewer_keywords: ["GetInterfaceSlot","GetInterfaceSlot method [Direct3D 11]","GetInterfaceSlot method [Direct3D 11]","ID3D11ShaderReflectionVariable interface","ID3D11ShaderReflectionVariable interface [Direct3D 11]","GetInterfaceSlot method","ID3D11ShaderReflectionVariable.GetInterfaceSlot","ID3D11ShaderReflectionVariable::GetInterfaceSlot","b13015c6-721f-9155-57ca-42f52d0e5885","d3d11shader/ID3D11ShaderReflectionVariable::GetInterfaceSlot","direct3d11.id3d11shaderreflectionvariable_getinterfaceslot"]
old-location: direct3d11\id3d11shaderreflectionvariable_getinterfaceslot.htm
tech.root: direct3d11
ms.assetid: f3b62396-0747-4396-ba86-9d50bfa8b529
ms.date: 12/05/2018
ms.keywords: GetInterfaceSlot, GetInterfaceSlot method [Direct3D 11], GetInterfaceSlot method [Direct3D 11],ID3D11ShaderReflectionVariable interface, ID3D11ShaderReflectionVariable interface [Direct3D 11],GetInterfaceSlot method, ID3D11ShaderReflectionVariable.GetInterfaceSlot, ID3D11ShaderReflectionVariable::GetInterfaceSlot, b13015c6-721f-9155-57ca-42f52d0e5885, d3d11shader/ID3D11ShaderReflectionVariable::GetInterfaceSlot, direct3d11.id3d11shaderreflectionvariable_getinterfaceslot
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ShaderReflectionVariable::GetInterfaceSlot
 - d3d11shader/ID3D11ShaderReflectionVariable::GetInterfaceSlot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ShaderReflectionVariable.GetInterfaceSlot
---

# ID3D11ShaderReflectionVariable::GetInterfaceSlot


## -description

Gets the corresponding interface slot for a variable that represents an interface pointer.

## -parameters

### -param uArrayIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the array element to get the slot number for.  For a non-array variable this value will be zero.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Returns the index of the interface in the interface array.

## -remarks

GetInterfaceSlot gets the corresponding slot in a dynamic linkage array for an interface instance.  The returned slot number is used to set an interface instance to a particular class instance.  See the HLSL <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class">Interfaces and Classes</a> overview for additional information.

This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.


#### Examples

Retrieving and using an interface slot
          


```

ID3D11ShaderReflectionVariable* pAmbientLightingVar = pReflector->GetVariableByName("g_abstractAmbientLighting");
g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);
g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, &g_pHemiAmbientLightClass );
g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass; 
...
pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );
      
```


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflectionvariable">ID3D11ShaderReflectionVariable Interface</a>
