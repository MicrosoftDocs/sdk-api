---
UID: NS:d3d11.D3D11_CLASS_INSTANCE_DESC
title: D3D11_CLASS_INSTANCE_DESC
author: windows-sdk-content
description: Describes an HLSL class instance.
old-location: direct3d11\d3d11_class_instance_desc.htm
old-project: direct3d11
ms.assetid: 8ed0e6dd-227b-4e15-b949-34086523f064
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 27ba9c43-314f-b252-fc98-8a27455ec5dd, D3D11_CLASS_INSTANCE_DESC, D3D11_CLASS_INSTANCE_DESC structure [Direct3D 11], d3d11/D3D11_CLASS_INSTANCE_DESC, direct3d11.d3d11_class_instance_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: D3D11_CLASS_INSTANCE_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D11.h
api_name:
-	D3D11_CLASS_INSTANCE_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

