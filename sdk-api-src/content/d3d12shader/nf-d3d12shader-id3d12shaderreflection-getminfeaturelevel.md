---
UID: NF:d3d12shader.ID3D12ShaderReflection.GetMinFeatureLevel
title: ID3D12ShaderReflection::GetMinFeatureLevel
author: windows-sdk-content
description: Gets the minimum feature level.
old-location: direct3d12\id3d12shaderreflection_getminfeaturelevel.htm
old-project: direct3d12
ms.assetid: DE1FC45B-DA2B-41B6-A732-62BA886F51C2
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetMinFeatureLevel, GetMinFeatureLevel method, GetMinFeatureLevel method,ID3D12ShaderReflection interface, ID3D12ShaderReflection interface,GetMinFeatureLevel method, ID3D12ShaderReflection.GetMinFeatureLevel, ID3D12ShaderReflection::GetMinFeatureLevel, d3d12shader/ID3D12ShaderReflection::GetMinFeatureLevel, direct3d12.id3d12shaderreflection_getminfeaturelevel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12shader.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D12_SHADER_VERSION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflection.GetMinFeatureLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12ShaderReflection::GetMinFeatureLevel


## -description


Gets the minimum feature level.
        


## -parameters




### -param pLevel [out]

Type: <b><a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a>*</b>

A pointer to one of the enumerated values in <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL</a>, which represents the minimum feature level.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/145F2CCB-C076-42BE-8AF4-74349CDF6B02">ID3D12ShaderReflection</a>
 

 

