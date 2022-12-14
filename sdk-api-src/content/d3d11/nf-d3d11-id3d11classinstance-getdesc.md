---
UID: NF:d3d11.ID3D11ClassInstance.GetDesc
title: ID3D11ClassInstance::GetDesc (d3d11.h)
description: Gets a description of the current HLSL class.
helpviewer_keywords: ["64584e80-07e5-d72e-198e-074e63a44c16","GetDesc","GetDesc method [Direct3D 11]","GetDesc method [Direct3D 11]","ID3D11ClassInstance interface","ID3D11ClassInstance interface [Direct3D 11]","GetDesc method","ID3D11ClassInstance.GetDesc","ID3D11ClassInstance::GetDesc","d3d11/ID3D11ClassInstance::GetDesc","direct3d11.id3d11classinstance_getdesc"]
old-location: direct3d11\id3d11classinstance_getdesc.htm
tech.root: direct3d11
ms.assetid: 5062595c-4152-4cfd-afcd-3e51d1087675
ms.date: 12/05/2018
ms.keywords: 64584e80-07e5-d72e-198e-074e63a44c16, GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11ClassInstance interface, ID3D11ClassInstance interface [Direct3D 11],GetDesc method, ID3D11ClassInstance.GetDesc, ID3D11ClassInstance::GetDesc, d3d11/ID3D11ClassInstance::GetDesc, direct3d11.id3d11classinstance_getdesc
req.header: d3d11.h
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ClassInstance::GetDesc
 - d3d11/ID3D11ClassInstance::GetDesc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11ClassInstance.GetDesc
---

# ID3D11ClassInstance::GetDesc


## -description

Gets a description of the current HLSL class.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_class_instance_desc">D3D11_CLASS_INSTANCE_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_class_instance_desc">D3D11_CLASS_INSTANCE_DESC</a> structure that describes the current HLSL class.

## -remarks

For more information about using the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a> interface, see
          <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking">Dynamic Linking</a>.
        

An instance is not restricted to being used for a single type in a single shader. An instance is flexible and can be used for any shader that used the same type name or instance name when the instance was generated.
        

<ul>
<li>A created instance will work for any shader that contains a type of the same type name.
            For instance, a class instance created with the type name <b>DefaultShader</b> would work in any shader that contained a type <b>DefaultShader</b> even though several shaders could describe a different type.
          </li>
<li>A gotten instance maps directly to an instance name/index in a shader.
            A class instance acquired using GetClassInstance will work for any shader that contains a class instance of the name used to generate the runtime instance, the instance does not have to be the same type in all of the shaders it's used in.
          </li>
</ul>
An instance does not replace the importance of reflection for a particular shader since a gotten instance will not know its slot location and a created instance only specifies a type name.
        

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>