---
UID: NF:d3d12shader.ID3D12FunctionReflection.GetResourceBindingDesc
title: ID3D12FunctionReflection::GetResourceBindingDesc
author: windows-sdk-content
description: Gets a description of how a resource is bound to a function.
old-location: direct3d12\id3d12functionreflection_getresourcebindingdesc.htm
tech.root: direct3d12
ms.assetid: DBABC959-0692-4DB9-9726-AFE6972A6B52
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetResourceBindingDesc, GetResourceBindingDesc method, GetResourceBindingDesc method,ID3D12FunctionReflection interface, ID3D12FunctionReflection interface,GetResourceBindingDesc method, ID3D12FunctionReflection.GetResourceBindingDesc, ID3D12FunctionReflection::GetResourceBindingDesc, d3d12shader/ID3D12FunctionReflection::GetResourceBindingDesc, direct3d12.id3d12functionreflection_getresourcebindingdesc
ms.topic: method
req.header: d3d12shader.h
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
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12FunctionReflection.GetResourceBindingDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12FunctionReflection::GetResourceBindingDesc


## -description


Gets a description of how a resource is bound to a function.
        


## -parameters




### -param ResourceIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based resource index.
          


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn960201(v=VS.85).aspx">D3D12_SHADER_INPUT_BIND_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dn960201(v=VS.85).aspx">D3D12_SHADER_INPUT_BIND_DESC</a> structure that describes input binding of the resource.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



A shader consists of executable code (the compiled HLSL functions) and a set of resources that supply the shader with input data. <b>GetResourceBindingDesc</b> gets info about how one resource in the set is bound as an input to the shader. 
          The <i>ResourceIndex</i> parameter specifies the index for the resource.
        




## -see-also




<a href="https://msdn.microsoft.com/F0BF4AA9-66D7-4A33-A51C-B03C1D61F537">ID3D12FunctionReflection</a>
 

 

