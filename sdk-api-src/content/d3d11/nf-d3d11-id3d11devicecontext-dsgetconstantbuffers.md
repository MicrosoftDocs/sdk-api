---
UID: NF:d3d11.ID3D11DeviceContext.DSGetConstantBuffers
title: ID3D11DeviceContext::DSGetConstantBuffers (d3d11.h)
author: windows-sdk-content
description: Get the constant buffers used by the domain-shader stage.
old-location: direct3d11\id3d11devicecontext_dsgetconstantbuffers.htm
tech.root: direct3d11
ms.assetid: 070b3c40-ddb2-4c13-b0a0-1451e00e0ae1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DSGetConstantBuffers, DSGetConstantBuffers method [Direct3D 11], DSGetConstantBuffers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DSGetConstantBuffers method, ID3D11DeviceContext.DSGetConstantBuffers, ID3D11DeviceContext::DSGetConstantBuffers, d030ed43-b3f5-78af-cbb4-0d04d0e441b5, d3d11/ID3D11DeviceContext::DSGetConstantBuffers, direct3d11.id3d11devicecontext_dsgetconstantbuffers
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
 - ID3D11DeviceContext.DSGetConstantBuffers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::DSGetConstantBuffers


## -description


Get the constant buffers used by the domain-shader stage.


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
 

 

