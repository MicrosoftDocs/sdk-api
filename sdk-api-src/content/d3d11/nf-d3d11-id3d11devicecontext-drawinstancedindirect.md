---
UID: NF:d3d11.ID3D11DeviceContext.DrawInstancedIndirect
title: ID3D11DeviceContext::DrawInstancedIndirect method
author: windows-driver-content
description: Draw instanced, GPU-generated primitives.
old-location: direct3d11\id3d11devicecontext_drawinstancedindirect.htm
old-project: direct3d11
ms.assetid: f40c662d-7cdc-4592-b8d5-72aad0b4dd53
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 2014c761-6e9c-961c-13a0-087ea9f94a6a, DrawInstancedIndirect method [Direct3D 11], DrawInstancedIndirect method [Direct3D 11], ID3D11DeviceContext interface, DrawInstancedIndirect,ID3D11DeviceContext.DrawInstancedIndirect, ID3D11DeviceContext, ID3D11DeviceContext interface [Direct3D 11], DrawInstancedIndirect method, ID3D11DeviceContext::DrawInstancedIndirect, d3d11/ID3D11DeviceContext::DrawInstancedIndirect, direct3d11.id3d11devicecontext_drawinstancedindirect
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DeviceContext.DrawInstancedIndirect
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::DrawInstancedIndirect method


## -description


Draw instanced, GPU-generated primitives.


## -parameters




### -param pBufferForArgs [in]

Type: <b><a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a>, which is a buffer containing the GPU generated primitives.


### -param AlignedByteOffsetForArgs [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset in <i>pBufferForArgs</i> to the start of the GPU generated primitives.


## -returns



Returns nothing.




## -remarks



When an application creates a buffer that is associated with the <a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a> interface that  <i>pBufferForArgs</i> points to, the application must set the <a href="d3d11_resource_misc_flag.htm">D3D11_RESOURCE_MISC_DRAWINDIRECT_ARGS</a> flag in the <b>MiscFlags</b> member of the <a href="https://msdn.microsoft.com/a5e470bb-011b-4a2a-96d6-cbf76fe12638">D3D11_BUFFER_DESC</a> structure that describes the buffer. To create the buffer, the application calls the <a href="https://msdn.microsoft.com/5aec93c5-12a1-4b4e-813e-ee1e85adbf14">ID3D11Device::CreateBuffer</a> method and in this call passes a pointer to <b>D3D11_BUFFER_DESC</b> in the <i>pDesc</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

