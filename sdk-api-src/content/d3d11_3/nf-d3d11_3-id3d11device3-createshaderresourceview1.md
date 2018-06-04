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

# ID3D11Device3::CreateShaderResourceView1


## -description


Creates a shader-resource view for accessing data in a resource.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

Pointer to the resource that will serve as input to a shader. This resource must have been created with the <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">
          D3D11_BIND_SHADER_RESOURCE</a> flag.


### -param pDesc1 [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/051F58C1-E3F3-4205-B834-7A14FEDFED2C">D3D11_SHADER_RESOURCE_VIEW_DESC1</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/051F58C1-E3F3-4205-B834-7A14FEDFED2C">D3D11_SHADER_RESOURCE_VIEW_DESC1</a> structure that describes a shader-resource view. Set this parameter to <b>NULL</b> to create a 
        view that accesses the entire resource (using the format the resource was created with).


### -param ppSRView1 [out, optional]

Type: <b><a href="https://msdn.microsoft.com/5AF5DCAC-2C3A-45A7-A165-3FBE3E0D5CAB">ID3D11ShaderResourceView1</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="https://msdn.microsoft.com/5AF5DCAC-2C3A-45A7-A165-3FBE3E0D5CAB">ID3D11ShaderResourceView1</a> interface for the created shader-resource view. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return <b>S_FALSE</b> if the other input parameters pass validation).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the shader-resource view.  See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> for other possible return values.




## -see-also




<a href="https://msdn.microsoft.com/0AA10851-0077-4075-BD41-72FCD7BC0556">ID3D11Device3</a>
 

 

