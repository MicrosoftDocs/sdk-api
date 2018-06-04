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

# D3D11_CLASS_INSTANCE_DESC structure


## -description


Describes an HLSL class instance.


## -struct-fields




### -field InstanceId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The instance ID of an HLSL class; the default value is 0.


### -field InstanceIndex

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The instance index of an HLSL class; the default value is 0.


### -field TypeId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The type ID of an HLSL class; the default value is 0.


### -field ConstantBuffer

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Describes the constant buffer associated with an HLSL class; the default value is 0.


### -field BaseConstantBufferOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The base constant buffer offset associated with an HLSL class; the default value is 0.


### -field BaseTexture

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The base texture associated with an HLSL class; the default value is 127.


### -field BaseSampler

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The base sampler associated with an HLSL class; the default value is 15.


### -field Created

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

True if the class was created; the default value is false.


## -remarks



The D3D11_CLASS_INSTANCE_DESC structure is returned by the <a href="https://msdn.microsoft.com/5062595c-4152-4cfd-afcd-3e51d1087675">ID3D11ClassInstance::GetDesc</a> method.

The members of this structure except <b>InstanceIndex</b> are valid (non default values) if they describe a class instance aquired using  <a href="https://msdn.microsoft.com/26e5b1c7-d7b7-413b-a072-33f8f5dd5d3f">ID3D11ClassLinkage::CreateClassInstance</a>.  The <b>InstanceIndex</b> member is only valid when the class instance is aquired using <a href="https://msdn.microsoft.com/055f1670-0643-4a0a-8411-ac8a62e98826">ID3D11ClassLinkage::GetClassInstance</a>.




## -see-also




<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

