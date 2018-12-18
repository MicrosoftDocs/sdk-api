---
UID: NF:d3d11shader.ID3D11ShaderReflection.GetMinFeatureLevel
title: ID3D11ShaderReflection::GetMinFeatureLevel
author: windows-sdk-content
description: Gets the minimum feature level.
old-location: direct3d11\id3d11shaderreflection_getminfeaturelevel.htm
tech.root: direct3d11
ms.assetid: b10eb64b-18ff-4248-be6e-a9c45bce3e99
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMinFeatureLevel, GetMinFeatureLevel method [Direct3D 11], GetMinFeatureLevel method [Direct3D 11],ID3D11ShaderReflection interface, ID3D11ShaderReflection interface [Direct3D 11],GetMinFeatureLevel method, ID3D11ShaderReflection.GetMinFeatureLevel, ID3D11ShaderReflection::GetMinFeatureLevel, b8d12499-79aa-f3e6-bdd4-5ce99f2fe7d3, d3d11shader/ID3D11ShaderReflection::GetMinFeatureLevel, direct3d11.id3d11shaderreflection_getminfeaturelevel
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
 - ID3D11ShaderReflection.GetMinFeatureLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ShaderReflection::GetMinFeatureLevel


## -description


Gets the minimum feature level.


## -parameters






#### - pLevel [out]

Type: <b><a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a>*</b>

A pointer to one of the enumerated values in <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a>, which represents the minimum feature level.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.




## -see-also




<a href="https://msdn.microsoft.com/a28cca72-7f2d-416a-bfa9-4d1f71fc98d5">ID3D11ShaderReflection Interface</a>
 

 

