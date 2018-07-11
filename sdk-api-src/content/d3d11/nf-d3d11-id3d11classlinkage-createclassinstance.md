---
UID: NF:d3d11.ID3D11ClassLinkage.CreateClassInstance
title: ID3D11ClassLinkage::CreateClassInstance
author: windows-sdk-content
description: Initializes a class-instance object that represents an HLSL class instance.
old-location: direct3d11\id3d11classlinkage_createclassinstance.htm
old-project: direct3d11
ms.assetid: 26e5b1c7-d7b7-413b-a072-33f8f5dd5d3f
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: 9738cc0b-0925-52a9-bcc7-e3e76bec3278, CreateClassInstance, CreateClassInstance method [Direct3D 11], CreateClassInstance method [Direct3D 11],ID3D11ClassLinkage interface, ID3D11ClassLinkage interface [Direct3D 11],CreateClassInstance method, ID3D11ClassLinkage.CreateClassInstance, ID3D11ClassLinkage::CreateClassInstance, d3d11/ID3D11ClassLinkage::CreateClassInstance, direct3d11.id3d11classlinkage_createclassinstance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11ClassLinkage.CreateClassInstance
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11ClassLinkage::CreateClassInstance


## -description


Initializes a class-instance object that represents an HLSL class instance.


## -parameters




### -param pClassTypeName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The type name of a class to initialize.


### -param ConstantBufferOffset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Identifies the constant buffer that contains the class data.


### -param ConstantVectorOffset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The four-component vector offset from the start of the constant buffer where the class data will begin. Consequently, this is not a byte offset.


### -param TextureOffset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The texture slot for the first texture; there may be multiple textures following the offset.


### -param SamplerOffset [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The sampler slot for the first sampler; there may be multiple samplers following the offset.


### -param ppInstance [out]

Type: <b><a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>**</b>


            The address of a pointer to an <a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a> interface to initialize.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            Returns S_OK if successful; otherwise, returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -remarks



Instances can be created (or gotten) before or after a shader is created. Use the same shader linkage object to acquire a class instance and create the shader the instance is going to be used in.


          For more information about using the <a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a> interface, see <a href="https://msdn.microsoft.com/2f5f7852-0f0a-4fad-a412-9a0d634c73b6">Dynamic Linking</a>.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>
 

 

