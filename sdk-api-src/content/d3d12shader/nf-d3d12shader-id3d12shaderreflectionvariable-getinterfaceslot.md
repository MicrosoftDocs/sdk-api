---
UID: NF:d3d12shader.ID3D12ShaderReflectionVariable.GetInterfaceSlot
title: ID3D12ShaderReflectionVariable::GetInterfaceSlot
author: windows-sdk-content
description: Gets the corresponding interface slot for a variable that represents an interface pointer.
old-location: direct3d12\id3d12shaderreflectionvariable_getinterfaceslot.htm
old-project: direct3d12
ms.assetid: 6CD169C7-0C6B-4EC8-BF57-96EE5065CC9D
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: GetInterfaceSlot, GetInterfaceSlot method, GetInterfaceSlot method,ID3D12ShaderReflectionVariable interface, ID3D12ShaderReflectionVariable interface,GetInterfaceSlot method, ID3D12ShaderReflectionVariable.GetInterfaceSlot, ID3D12ShaderReflectionVariable::GetInterfaceSlot, d3d12shader/ID3D12ShaderReflectionVariable::GetInterfaceSlot, direct3d12.id3d12shaderreflectionvariable_getinterfaceslot
ms.prod: windows
ms.technology: windows-sdk
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
 - ID3D12ShaderReflectionVariable.GetInterfaceSlot
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12ShaderReflectionVariable::GetInterfaceSlot


## -description



          Gets the corresponding interface slot for a variable that represents an interface pointer.
        


## -parameters




### -param uArrayIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            The index of the array element to get the slot number for.
            For a non-array variable this value will be zero.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Returns the index of the interface in the interface array.
          




## -remarks



GetInterfaceSlot gets the corresponding slot in an dynamic linkage array for an interface instance.
          The returned slot number is used to set an interface instance to a particular class instance.
          See the HLSL <a href="https://msdn.microsoft.com/124a358d-30ab-4efe-88ed-1ff277d17b25">Interfaces and Classes</a> overview for additional information.
        


        This method's interface is hosted in the out-of-box DLL D3DCompiler_xx.dll.
      




## -see-also




<a href="https://msdn.microsoft.com/E4CF0C77-2792-46DC-B38F-22C0ACBFD615">ID3D12ShaderReflectionVariable</a>
 

 

