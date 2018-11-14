---
UID: NF:d3d11.ID3D11DeviceContext.HSGetConstantBuffers
title: ID3D11DeviceContext::HSGetConstantBuffers
author: windows-sdk-content
description: Get the constant buffers used by the hull-shader stage.
old-location: direct3d11\id3d11devicecontext_hsgetconstantbuffers.htm
tech.root: direct3d11
ms.assetid: 82987afa-fcb4-4d87-ab53-916a9dac3609
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 46eee6d7-9ce0-ef7b-68bd-2f0c8f0b3136, HSGetConstantBuffers, HSGetConstantBuffers method [Direct3D 11], HSGetConstantBuffers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],HSGetConstantBuffers method, ID3D11DeviceContext.HSGetConstantBuffers, ID3D11DeviceContext::HSGetConstantBuffers, d3d11/ID3D11DeviceContext::HSGetConstantBuffers, direct3d11.id3d11devicecontext_hsgetconstantbuffers
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.HSGetConstantBuffers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11DeviceContext.HSGetConstantBuffers
: 
---

# ID3D11DeviceContext::HSGetConstantBuffers


## -description


Get the constant buffers used by the <a href="https://msdn.microsoft.com/4ad2fd3e-6e1a-4326-8469-3198acf931dc">hull-shader stage</a>.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into the device's zero-based array to begin retrieving constant buffers from (ranges from 0 to D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT - 1).


### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of buffers to retrieve (ranges from 0 to D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT - StartSlot).


### -param ppConstantBuffers [out, optional]

Type: <b><a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a>**</b>

Array of constant buffer interface pointers (see <a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a>) to be returned by the method.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

